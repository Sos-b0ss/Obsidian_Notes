Sources:

\
[MongoDB is](https://www.mongodb.com/) a document-oriented [NoSQL database](https://www.howtogeek.com/devops/what-is-a-nosql-database-and-what-are-they-good-for/) engine that’s gained popularity with developers for its [[JSON]]-like storage model. [[MongoDB]] often provides a more direct mapping between code and persisted data, facilitating rapid iteration and helping address the sizable [impedance mismatch](https://www.howtogeek.com/devops/whats-an-impedance-mismatch-in-programming/) of traditional [[SQL]] [[database]]s.
\
[[Docker]] is a platform that packages your application components as isolated containers. [[Container]]izing your [[MongoDB]] [[Database]] makes it portable across environments, letting you spin up an instance anywhere [[Docker]] is available.
\
In this guide, we’ll show you how to get started running [[MongoDB]] in [[Docker]]. The key consideration is data storage: [[Docker]] containers are [[Ephemeral]] by default and lose their data when they stop. You’ll need to mount [a volume](https://www.howtogeek.com/devops/what-are-docker-volumes-and-how-do-you-use-them/) into your [[MongoDB]] container to enable persistence.

## Starting a MongoDB Container

You can start a throwaway [[MongoDB]] [[container]] with 'docker run':

```
docker run -d -p 27017:27017 --name example-mongo mongo:latest
```

This will give you a live server running the latest version of MongoDB. It uses the official image available [on Docker Hub](https://hub.docker.com/_/mongo). The '-d' (detach) flag means the container will run in the background, separately to your shell process.
\
The container port '27017', the MongoDB default, is bound back to port '27017' on your host. You’ll be able to connect to your Mongo instance on 'localhost:27017'. If you want to change the port number, modify the first part of the '-p' flag, such as '9000:27017' to use 'localhost:9000'.
\
The MongoDB image also includes the 'mongo' shell. The [`docker exec`](https://www.howtogeek.com/devops/how-to-run-a-command-on-a-running-docker-container/) command provides a way to access it in a running container:
\
```
docker exec -it example-mongo mongo
```
\
This will launch an interactive [Mongo shell session](https://docs.mongodb.com/v4.4/mongo) in your terminal. It’s ideal for quickly interacting with your database instance without adding any external dependencies.

![image of using the Mongo shell in Docker](https://www.howtogeek.com/wp-content/uploads/csit/2021/11/00bf23e1.png?trim=1,1&bg-color=000&pad=1,1)

You can inspect Mongo’s logs with the [`docker logs` command](https://www.howtogeek.com/devops/how-to-monitor-docker-container-logs/):

```
docker logs example-mongo --follow
```

The '--follow' flag means logs will be continually streamed to your terminal.

## Connecting From Another Container

If you’re deploying Mongo in Docker, chances are you’ll be wanting to connect from another container such as your API server. It’s best to join both to a shared Docker network. This means you won’t need to publish Mongo ports to your host, reducing your attack surface.

docker network create mongo-network
docker run -d --network mongo-network --name example-mongo mongo:latest

Your “client” container should join to the 'mongo-network' too. It’ll be able to reference the container by name within MongoDB connection strings. In this example, it could reach the database by contacting 'example-mongo:27017'.

## Persisting Data With Volumes

You must use [[Docker]] volumes if you’ll be hosting a real database in your Mongo container. Using a volume persists your data so it’s not lost when you stop the container or restart the [[Docker]] [[Daemon]].

The MongoDB image is configured to store all its data in the '/data/db' directory in the container filesystem. Mounting a volume to this location will ensure data is persisted outside the container.
```

docker run -d 
    -p 27017:27017 
    --name example-mongo 
    -v mongo-data:/data/db 
    mongo:latest
```
```
This version of the `docker run` command creates a new Docker volume called `mongo-data` and mounts it into the container. The volume will be managed by Docker; you can see it by running `docker volumes ls`.

Add some data to Mongo:

```use test-db
db.demos.save({foo: "bar"})
```

Next restart your container:

```
docker restart example-mongo
```


The previously added data will remain intact as Docker reattaches the volume after the restart. You can check this by reconnecting to Mongo and querying the 'demos' collection:

```
use test-db
db.demos.find({foo: "bar"})
```

You can remove the container and run an entirely new one with the same 'mongo-data' volume. As the volume’s files will still exist on your host, Docker will mount them back into the replacement container. Mongo automatically skips its usual database initialization routine when the data directory is already populated at container startup.

[[Volume]]s persist until you remove them with the 'docker volumes' rm command or use the --'volumes' flag when destroying a container with [`docker rm`](https://docs.docker.com/engine/reference/commandline/rm).

## Adding Authentication

Fresh MongoDB containers lack authentication so anyone can connect to your server. Don’t expose the container’s ports on a networked system that an attacker could access. Mongo’s authentication system should be used to properly secure your database.

The Mongo Docker image provides a convenient quickstart for Mongo’s relatively complex [authentication system](https://docs.mongodb.com/manual/reference/program/mongod/#cmdoption-mongod-auth). You can add an initial user account by setting the 'MONGO_INITDB_ROOT_USERNAME' and 'MONGODB_INITDB_ROOT_PASSWORD' environment variables when you create your container:

```
docker run -d 
    -p 27017:27017 
    --name example-mongo 
    -v mongo-data:/data/db 
    -e MONGODB_INITDB_ROOT_USERNAME=example-user 
    -e MONGODB_INITDB_ROOT_PASSWORD=example-pass 
    mongo:latest
```

This will start the database with a new user account called 'example-user'. The user will be assigned the 'root' role in the 'admin' authentication database, granting [[Superuser]] privileges.

Considering the powers associated with this account, providing its password as a plain-text environment variable can be problematic. A more secure approach is to inject the password as a file:

```
docker run -d 
    -p 27017:27017 
    --name example-mongo 
    -v mongo-data:/data/db 
    -e MONGODB_INITDB_ROOT_USERNAME=example-user 
    -e MONGODB_INITDB_ROOT_PASSWORD_FILE=/run/secrets/mongo-root-pw 
    mongo:latest
```

Suffixing the image’s environment variables with '_FILE' instructs Mongo to read the contents of the referenced file, instead of using the value as-is. The actual file path is arbitrary – either mount a file from your host machine or use [Docker Secrets](https://www.howtogeek.com/devops/how-to-secure-sensitive-data-with-docker-compose-secrets/). Either way, your password won’t be visible when using ''docker inspect'' to view the container’s variables.

## Configuring Your Server

The easiest way to supply custom Mongo config values is to use the flags offered by [the `mongod` binary](https://docs.mongodb.com/manual/reference/program/mongod/#core-options). The Docker image is preconfigured to pass [its `docker run` flags](https://www.howtogeek.com/devops/the-difference-between-cmd-and-entrypoint-in-docker-images/) through to ''mongod''.
\
Here’s an example where Mongo is [set to listen on](https://docs.mongodb.com/manual/reference/program/mongod/#std-option-mongod.--port) port '9000' instead of the default '27017':

```
docker run -d 
    --name example-mongo 
    -v mongo-data:/data/db 
    mongo:latest --port 9000
```

You can add a Mongo config file by mounting one into your container, then using the '--config' flag to tell Mongo where to look:

```
docker run -d 
    --name example-mongo 
    -v mongo-data:/data/db 
    -v ./mongo.conf:/etc/mongo/mongo.conf
    mongo:latest --config /etc/mongo/mongo.conf
```

The '--config' flag must be used – Mongo doesn’t load settings from any file path by default.
\
The Docker image provides a mechanism to seed your database and run bootstrap scripts on first run. Any `.sh` or `.js` files placed in the '/docker-entrypoint-initdb.d' directory will be executed in alphabetical order. `.js` files will be treated as Mongo scripts and run against the 'test' [[Database]]. You can change this default database by setting the `MONGODB_INITDB_DATABASE` environment variable to a custom schema name.

## Conclusion

Running MongoDB in Docker gives you isolation and portability for your database. You can quickly spin up new instances without manually installing the Mongo [[Server]]. Your application containers can link directly to Mongo over a shared [[Docker_Network]].

The Mongo image on Docker Hub has [tags for](https://hub.docker.com/_/mongo?tab=tags) all actively supported versions including 4.4 [and 5.0](https://www.howtogeek.com/devops/whats-new-in-mongodb-5-0/). The 'latest' tag always points to the newest release, currently '5.0', so using it puts you at risk of receiving unwanted major version bumps. It’s safer to indicate a specific version when starting your containers.

The official image can also be used as the base for custom preconfigured ones. Building a '[[Dockerfile]]' that adds your config file, overrides the 'COMMAND' to include it, and copies in your seeding scripts would give you a way to bring up a new database instance with fewer 'docker run' flags.
