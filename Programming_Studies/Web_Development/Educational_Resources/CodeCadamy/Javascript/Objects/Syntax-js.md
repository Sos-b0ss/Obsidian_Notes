~objects are containers that store data & functions (it isn't ordered, only way to access is with calling its associated key.)  
  \
ex of object syntax:  
let restaurant = { //creates variable named restaurant it holds the object in the {}  
name: 'Italian Bistro',  
seatingCap: 120, //name, seatingCap, etc.. all are keys of the object  
hasDineInSpecial: true, //seperate all keys and values with a colon  
entrees: ['penne alla bolognese', 'chicken cacciatore', 'linguine pesto']  
}; // keys can be ANY DATA TYPE, including OTHER OBJECTS  
  \
~ How to access the keys' values in objects:  
use 'Dot notation'  
ex: console.log(restaurant.entrees);  
(output would be the whole entree array)  
or,  
'Bracket notaton'  
ex: console.log(restaurant ['entrees']);  
(same output as 'Dot notation')  
  \
~ the benefit of bracket notation is you can use variables inside the brackets to select the keys of an object.  
ex: A restaurant my have a different special for each time of day. you can put each special inside the "resaurantSpecials" object, then select one we need later in our program based on the current time.  
  \
ex code using syntax:  
let meal = 'none';  
let time = 12;  
//using military time  
const restaurantSpecials = {  
breakfast: 'The breakfast special YUM!',  
lunch: 'mmm burgers, for lunch MURICA',  
none: 'we got nothing fool'  
};  
  \
if ( time < 11 ) { //11 AM  
meal = 'breakfast';  
} else if ( time < 17 ) { //5PM  
meal = 'lunch';  
}  
  \
console.log(restaurantSpecials[meal]);  
  \
Code would return:  
The breakfast special YUM!
