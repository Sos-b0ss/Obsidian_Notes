When using a .forEach Iterator with a function, such as:  
\
let groceries = ['food'];  
groceries.forEach(function(groceryItem) {  
console.log(' - ' + groceryItem);  
});  
\
The parameter "groceryItem" will contain every element in the "groceries" array as the method .forEach iterates the function.  
Once the Iterator is completed it returns with "undefined"
