Helps devs know where a var can be used in a program. there's 2 kinds of scope:  
~ Global Scope - stars in nights sky; everyone can see them  
~ Block Scope - river and cityline, only you and your city can see this, however you can still see the stars.  
  \
{ } = Block, so any variable declared outside is considered a global variable.  
ex: const colour = 'blue;  
const colourOfSky - ( ) => {  
return colour;  
};  
console.log(colourOfSky( )); //Going to return the string "blue"  
  \
- the var colour is global and can be used in any blocks.  
(* Remember the function syntax:  
function myNightSky () {  
return 'Night Sky:' + satellite + ', ' + stars + ', ' + galaxy;  
}  
OR alternativly you can use string interpolation in the function:  
return `Night Sky: ${satellite}, ${stars}, ${galaxy}`;  
)
