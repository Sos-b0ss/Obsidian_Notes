~ If you want a seperate file to handle the processes you just created a seperate file and import the object that was ".exports" using require()  
ex: const Menu = require('/Menu.js');  
function placeHolder() {  
console.log(`My order is: ${Menu.Specialty}`);  
}  
PlaceHolder();  
_______________________________________________________________  
  
Exports II:  
  
~ You can wrap any collection of data together (or functions) export them.  
ex: let Menu;  
module.exports = {  
specialty = "Roasted Beets",  
getSpecialty + function() {  
return this.specialty;  
}  
};  
then to require you write:  
const Menu = require ('./Menu.js');  
console.log(Menu.getSpecialty());