Sources:

\
Examples of Key-value databases: [[Redis]], [[Memcached]], [[Etcd]]
\
The data base is structured almost like a [[JavaScript]] object, or a [[Python]] Dictionary.
\
You have a key, where every key is unique, and those all point to some value. 
With Redis for example, we can read and write data, using commands:

---

ex.
	redis > SET user:23:bio "i like turtles"
	>> OK
\
	redis > GET user:23:bio
	>> "i like turtles"

---

Here you used the SET command with a key and a value to write the data, and the get command to retrieve that data in the future.
\
In the case with [[Redis]], and [[Memcached]], all the data is held in the machines memory. As apposed to most other data bases that keep all their data on the disk.
\
This limits the amount of data you can store, however makes the database extremely fast because it doesn't require a round trip to the disk for every operation. In addition it doesn't preform queries, joins or anything like that so the data modelling options are very limited, however it makes up for that in times because of how fast it is.
\
Big apps like to use this form of database for real time delivery of their data, however it isn't used for their long term data. So as to treat it more like a cache.
\
What are these data bases best at?:
Caching
Pub/Sub
Leaderboards

---

![[Pasted image 20220626195019.png]]

---

As you can see here its fairly useful to use this form of data base on top of some other persistent database layer. So this makes Key-value databases fairly limited on their own.
