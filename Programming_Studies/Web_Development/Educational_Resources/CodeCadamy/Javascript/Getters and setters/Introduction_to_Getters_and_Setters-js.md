~ 'Getter' and 'Setter' methods get and set the properties inside of an object. This is good because you can:  
-Check if new data is valif before setting a property.  
-Preform an action on the data while you are getting or setting a property.  
-Control which properties can be set and retrieved.  
ex:  
let restaurant = {  
_name: 'You know',  
_seatingCapacity: 120,  
_entrees: ['cheese','lots of cheese']  
  
set seatingCapacity(newCapacity) {  
if {typeof new Capacity === 'number') {  
this._seatingCapacity = newCapacity;  
console.log(`${newCapacity} is valid imput.`);  
} else {  
console.log(`Change ${newCapacity} to a number.`)  
}  
}  
}  
  
~ Using a "_" before a prop name indicates that it should not be modified directly by other code.  
~ Instead put a "_" before all properties and create setters for all attributes you want to access later in the code.

Getters Continued
---
~ Used to 'get' the property values inside an objject.  
ex: get seatingCapacity() {  
console.log(`There are ${this._seatingCapacity} seats at the restaurant.`);  
return this._seatingCapacity;  
} // get seatingCapacity() logs something & returns the value saved to //_seatingCapacity  
}  
~ you call a getter method the same way you would access a property without a method:  
restaurant.seatingCapacity = 150;  
const seats = restaurant.seatingCapacity;

Setters Continued
---
~How to cal a setter method:  
restaurant.seatingCapacity = 150;  
(this would make the output of the code:  
" 150 is valit input. for the example code of:  
let restaurant = {  
_name: 'You know',  
_seatingCapacity: 120,  
_entrees: ['cheese','lots of cheese']  
  
set seatingCapacity(newCapacity) {  
if {typeof new Capacity === 'number') {  
this._seatingCapacity = newCapacity;  
console.log(`${newCapacity} is valid imput.`);  
} else {  
console.log(`Change ${newCapacity} to a number.`)  
}  
}  
} "  
  
~ This set _seatingCapacity value to 150. See how it used the same syntax to set a property that doesn't have a setter method.  
(because '150' is a number it returned the first block in the if statement and changes _seatingCapacity)  
(ps it's just using dot notation in case you forgot)