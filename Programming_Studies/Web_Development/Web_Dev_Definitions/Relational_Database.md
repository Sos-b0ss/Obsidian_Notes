Sources:

\
Examples of relational databases: [[MySQL]], [[Programming_Studies/Web_Development/Web_Dev_Definitions/PostgreSQL]], [[SQLserver]]
\
Been around for nearly 50 years, and continue to be one of the most popular types of databases in the world.
\
Was the building block that helped inspire [[SQL]].
\
![[Pasted image 20220626202610.png]]
\
Easy way to think of it is:
\
Imagine you have a facility, and on that facility you build airplanes. The facility is the database, and on that data base you might have different warehouses that hold different parts like engines, wheels, and so on. Each warehouse is like a database table for holding a certain type of part, each individual part has a serial number to uniquely identify it, and you can think of an individual part as a row in a table.
\
So now that you have all these parts separated into different warehouses, how do you build an airplane. That's where relationships come in. You can build an airplane by referencing the unique ID of the different parts that go into it. Notice how each part has its own unique ide, this is known as its primary key, and it defines its various parts by referencing their IDs, those are known as foreign keys, because they reference data in a different table.
\
Now if we want to join all this data together, were going to want to run a query, to do that.
\
Main take away is that an [[SQL]] database organizes data in its smallest normal form.

![[Pasted image 20220626203255.png]]

	^^^Foreign key ................................ ^^^Primary keys

---

A potential drawback is that it requires a [[Schema]]. If you don't know the right data shape up front, they can be a little harder to work with. 
\
[[SQL]] [[Database]]s are also [[ACID]] compliant. Which means whenever there's a transaction in the database, data validity is guaranteed, even if there are network or hardware failures. This is essential in banks and financial institutions, but it makes this type of database inherently more difficult to scale.
\
However there are more modern [[SQL]] [[Database]]s like [[CockroachDB]], that are specifically designed to operate at scale. 
\
Relational databases are best for:
- Most apps
\
But isn't very good at:
- Unstructured data
\
