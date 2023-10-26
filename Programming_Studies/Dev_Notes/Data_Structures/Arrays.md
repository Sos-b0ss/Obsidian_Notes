**Simple Explanation:**
\
A continuous block of cells in the computer's memory. By keeping track of its memory location, (Say the location is 1000 for example), it can instantly compute the location of any item inside of it. For example if we want to get index number 5 here:
```
v----- location '1000'
[ 5, 6, 7, 8, 9, 10 ]
				 ^----- location '1005'
```

Then we would just add '5' to '1000', get the result of '1005' then we can just pull that value directly which in this case would be '10'
\
**Pros:**
- Arrays are really good at retrieving items.

**Cons:**
- If your array keeps growing in size it could start running into other things in memory, so always adding isn't nearly as efficient because to avoid this from happening you will need to start adding the array somewhere else in memory entirely to make it fit (Like in scripting languages such as Js & Python). However in lower level languages you have to declare the size of your array in advance.


---

**Complex Explanation:**
