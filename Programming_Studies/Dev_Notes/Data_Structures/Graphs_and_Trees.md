**Simple Explanation:**
\
The topic of 'Graphs' in particular is so massive that there is an entire field in computer science called [[Graph_Theory]]. What a graph is, is pretty similar to a linked list, where you have nodes that are pointing to other nodes, except in this case the pointers are called `edges`. Edges can also have what are called `weights` (basically numbers) assigned to them. Imagine you have two cities, like Phoenix and Portland, and the road that connects the two of them is the edge and the length of that road in miles would be the weight of that edge. Complicated relationships like social media networks are also stored as graphs.
\
Trees are a special kind of a hierarchical graph, in which the data expands out in one direction. We can use these to represent a lot of things, like a family tree, or even an HTML tree with nested elements.
\
There's an even more specific tree called a [[Binary_Search_Tree]]. This tree has really specific rules but these rules allow us to do things like searching really efficiently. The rules are as follows:
1. Each node can only have at maximum 2 children (0-2) which are Left, and Right.
2. The Left node has to be less than the node. (Left < node)
3. The Right one has to be more than the node. (Right > node)

With these rules in place, we can traverse through the tree and always know where an element is. So if you had a 5 at the top and you were looking for 7 you would know its either to the right or not in the tree at all.
\
Unfortunately [[BST]] is not a perfect data structure either, if you add elements in a weird order, you get very unbalanced or one sided, and that effectively loses you all the advantages of search optimization. (There are self balancing trees like [[Red_Black_Trees]], [[B_Trees]]), but thats getting into more advanced data structures.

---

**Complex Explanation:**
