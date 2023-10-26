Sources:

\
Examples of Graph databases: [[Neo4j]], [[DGraph]]
\
![[Pasted image 20220626204548.png]]
\
Imagine you don't want to model a relationship and a schema and wanted to just treat the relationship itself as data.
\
Data is represented as nodes, and the relationships between them as edges.
This is useful for any situation that you may want a many to many relationship 
\
In an SQL database you set up a join table, with the foreign keys that define the relationship.
\
With a graph database, you don't need this middle man table, you just define an edge and connect it to the other record.
\
Here's the difference between Relational and graph databases illustrated:
\
![[Pasted image 20220626204826.png]]

---

You can now query the data with a statement that's much more precise and readable, in addition you can achieve much better performance, especially on larger datasets.
\
![[Pasted image 20220626205203.png]]
\
Graph databases can be a great alternative to SQL especially if your running a lot of joins and performance is taking a hit because of that. They're often used in fraud detection in finance, for building internal knowledge graphs in companies, and to power recommendation engines like the one used in Airbnb.
\
Graph Databases are best for:
- Graphs!
- Knowledge Graphs
- Recommendation Engines
