Sources:

\
Examples of Wide Column databases: [[Cassandra]], [[Hbase]]
\
![[Pasted image 20220626195441.png]]

---

Wide column databases are like if you took a key value data base and added a second dimension to it.
At the outer layer you have a [[Keyspace]], which holds 1 or more column families, and each column family holds a set of ordered rows. This makes it possible to group related data together.
But unlike a relational database, it doesn't have a schema so it can handle unstructured data.

---

An example of this in CQL (Cassandra Query Language):
![[Pasted image 20220626195819.png]]

---

This is nice for devs because you get a language called [[CQL]] which is very similar to [[SQL]] although much more limited and you cannot do joins. However its much easier to scale up, and replicate data across multiple notes. Unlike an [[SQL]] database, its decentralized, and can scale horizontally. 

--- 
![[Pasted image 20220626200038.png]]

---

Popular use cases are for scaling a large amount of time series data, like records from an [[IOT]] device, Weather sensors, or in the case of Netflix, a history of the different shows you've watched. Its normally used in spaces where you have frequent writes, but infrequent updates and reads.

So Wide Column data bases are best for:
- Time-Series
- Historical records
- High-Write, Low-Read
