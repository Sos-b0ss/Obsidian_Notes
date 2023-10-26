~ ex of getters and methods in a class:  
class Dog {  
constructor(name) {  
this._name = name;  
this._behaviour = 0;  
}  
get name() {  
return this._name;  
}  
get behaviour() {  
return this._behaviour;  
}  
incrementBehaviour {  
this._behaviour++;  
}  
}  
  
~ See no commas separating the methods  
~ Also we dont want them to be referenced directly.  
  \
ex of creating two dogs instances and calling methods on both;  
  \
let nikko = new Dog('Nikko') // creates new dog named Nikko  
nikko.incrementBehaviour(); // adds one to Nikko's behaviour  
let bradford - new Dog('Bradford'); // creates a new dog  
console.log(nikko.behaviour); // logs '1' to the console.  
console.log(bradford.behaviour); // logs '0' to console.
