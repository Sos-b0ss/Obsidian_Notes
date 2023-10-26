Sources:

\
Example of Multi-model databases: [[FaunaDB]]
\
![[Pasted image 20220626210558.png]]
\
Very different than anything that's been looked at so far with the other types of databases in this index.
\
Normally if all you want to worry about is some [[JSON]], than with [[FaunaDB]], you don't have to worry about things like, data modeling, schemas, replication, shards, or anything like that. 
\
With Fauna DB you describe how you want to access your data, using [[GraphQL]] like here:
\
![[Pasted image 20220626210944.png]]
\
Here we have a user model, and a post model, where a user can have many posts.
If you then upload that [[GraphQL]] schema to [[FaunaDB]] it will automatically create collections where you can store data, and an index to query the data. Behind the scenes its figuring out how to use multiple different database paradigms, like graph, relational, and document. It then determines how best to use these paradigms based on the the [[GraphQL]] code that was provided. You create data by adding documents to collections just like you would with a document database, but you're not stuck with the inherent limitations of data modeling. On top of that, it's [[ACID]] compliant, extremely fast, and you never have to worry about provisioning the actual infrastructure. You just decide how you want to consume your data, and you let the cloud figure everything else out for you.
\
![[Pasted image 20220626211429.png]]
\
Multi-model databases are best at:
- Everything?
