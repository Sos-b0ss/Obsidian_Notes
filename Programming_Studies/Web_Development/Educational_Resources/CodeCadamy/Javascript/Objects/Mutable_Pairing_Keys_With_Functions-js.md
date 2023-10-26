~ objects are considered mutable which means you can change them after they've been created (using Dot notation or bracket)  
  \
ex: const restaurant = {  
name: 'Italian Bistro',  
seatingCapacity: 120,  
hasDineInSpecial: true  
}  
  \
~ all you need to write to add a key to the object is:  
restaurant['appetizers'] = ['fried calamari', 'Bruchetta'];  
restaurant.desserts = ['HomemadeTiramiso, 'Cannoli']  
  \
(These are now both a part of the 'restaurant' object)  
  \
~ this also means you can use theses same operators to edit what is already assigned to the object.  
  \
~pairing keys with functions:  
  \
you can do this with arrow syntax by simply declaring a function inside an object as a key:  
ex: closeRestaurant: ( ) => {  
return 'Lock door, plant C4, run like hell.'  
}
