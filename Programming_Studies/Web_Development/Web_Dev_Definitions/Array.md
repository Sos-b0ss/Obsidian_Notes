Sources:

\
In Javascript:
---
It is always required to have a parameter such as "word" in the function:  
let betterWords = storyWords.filter(function(word){  
‎if (!unnecessaryWords.includes(word)){  
‎return word;  
‎}  
‎});  
‎In this example function the method .filter is used to iterate through the array "storyWords". As it goes through the if statement it checks if "word" being in the array unnecessaryWords evaluates to false because of the "!". If the parameter "word" passes through and is not contained in the array then it returns whatever element is contained in "word".

---
