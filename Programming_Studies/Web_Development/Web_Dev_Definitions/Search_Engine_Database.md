Sources:

\
Examples of Search Engine Databases: [[ElasticSearch]], [[Solr]], and cloud based options like [[Algolia]], [[MeiliSearch]]
\
This would be useful for creating something like google. Where a user provides a small amount of text, then your database needs to return the most relevant results in the proper order, from a huge amount of data. For that you'll be needing to put together a [[Fullstack_Framework]] search engine. 
\
![[Pasted image 20220626205632.png]]
\
Most of these databases are based on top of the [[Apache_Lucene]] project, which has been around since 1999.
\
These work very similar to a document oriented database. You start with an index, then you add a bunch of data objects to it. The difference is that under the hood, the search database will analyze all the text in the document and create an index of the searchable terms. So essentially they work like the index that you'd find in the back of a textbook. When a user preforms a search, it only has to scan the index, rather than every document in the database. That makes it very fast even on large datasets. The database can also run a variety of different algorithms to rank those results, filter out irrelevant hits, handle typos, and so on. This does add a lot of overhead and can be expensive to run at scale, but at the same time they can add a ton of value to the user experience if your using something like a type ahead search box.
\
Search engine databases are best for:
- Search engines
- Type Ahead
