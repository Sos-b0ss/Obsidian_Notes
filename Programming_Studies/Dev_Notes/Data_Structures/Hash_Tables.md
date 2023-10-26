**Simple Explanation:**
\
These are things like 'Objects' in Js, or a 'dict' in Python. In a situation like this a dictionary is a great word to use as an example because its like you give the hash table a word (or a key) like: `jerry["height"]` and it will return the definition (or the value) for you like `35`. Under the hood it works a lot like an array, the key actually gets run through a function called a [[Hashing_Function]], and that will spit out a memory location for you. The way its different though is the memory locations don't have to be next to each other, they can be anywhere. So you dont have the same problem with the size increasing. There is however a different problem depending on the hashing algorithm you use two keys could hash to the same memory location, which is known as a [[Hash_Collision]], and there are different ways to resolve this, but again in high level languages its all happening under the hood.
\
**Pros:**
- Adding and Removing
- Retrieving

**Cons:**
- Possibility of key collisions could be catastrophic


---

**Complex Explanation:**
