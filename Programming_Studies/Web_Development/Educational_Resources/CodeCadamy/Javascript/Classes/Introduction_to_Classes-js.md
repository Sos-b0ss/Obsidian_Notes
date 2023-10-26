~ Useful syntax that will help make multiple object have the same properties.  
~ will also learn about inheritance - used to efficiently create classes with similar properties.  
(Classes are great tools to avoid duplicate code and saves time debugging.)  
  \
ex class:  
class Dog {  
constructor(name) {  
this._name = name;  
this.behaviour = 0;  
}  
get name() {  
return this._name;  
}  
get behaviour() {  
return this._behaviour;  
}  
incrementBehaviour() {  
this._behaviour ++;  
}  
}  
*JS calls the "contructor" method every time it creates a new instance of a class.

---
~ Always capitalize and camelCase class names.  
  
~ Instances: a class instance is an object that contains the property names and methods of a class but with unique property values  
ex:  
class Dog {  
constructor(name) {  
[this.name](http://this.name/) = name;  
this.bahviour = 0;  
}  
}  
const halley - new Dog('Halley'); // creates instance new dog  
console.log(halley.name);  
//this will log the 'name' value saved to halley  
//OUTPUT: 'Halley'  
~ You use the 'new' keyword to create an instance of the Dog class.  
(it calls the 'constructor()', runs the code inside of it, and then returns the new instance.)  
~ this all works very well with getters, setters, and methods.  
~Class method and getter syntax is the same as it is for objects *except you CANT include commas between methods*