Sources:

\
Examples of Document databases: [[MongoDB]], and [[Firestore]], [[DynamoDB]], [[CouchDB]]

---

![[Pasted image 20220626200604.png]]

Most often used for primary app databases.

---

In this type of database you have documents, where each document is a container for key-value pairs. They're unstructured and don't require a schema, and the documents are grouped together in collections. 
\
Fields within a collection can be indexed, and collections can be organized into a logical hierarchy. This allows you to model retrieve relational data to a pretty significant degree.
\
They don't support joins, so instead of normalizing your data into a bunch of small parts, you're encourages to embed your data into a single document. 
\
\
Tradeoffs:
- Schema-less [+]
- Relational-ish queries [+]
- without joins [-]
\
![[Pasted image 20220626201447.png]]
\
![[Pasted image 20220626201511.png]]

---

This creates a tradeoff, where reads from a front end application are much faster, however writing or updating data tends to be more complex.

![[Pasted image 20220626201009.png]]

---

Document databases are far more general purpose than the other options so far. 
\
They kind of fall apart when you have a bunch of disconnected but related data that is updated often, like a social app that have many users, that have many comments, that have many likes, and you want to see all the comments that your friends like. Data like this needs to be joined, and its not easily done in a document database at scale.
\
From a developers perspective, they're very easy to use.
\
Document data bases are best used for:
- Most apps
- Games
- IOT
