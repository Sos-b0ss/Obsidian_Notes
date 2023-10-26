Functions can also be written like:  
\
ex:  
const myNightSky = ( ) => {  
//blah, blah  
};  
Global Scope - It can kinda be pretty bad to have every variable be declared globally, it can collide with other code and do some funky stuff you dont want.  
  \
Block scope is power in js, it allows us to define variables with precision, and not pollute the global name space.  
  \
~ In this example code it displays how a variable will be set to two different strings but will not tie them to that string exclusively because on is declared inside of a block and exuded from the global namespace like stated above:  
const visibleLightWaves = ( ) => {  
let visibleLightWaves = 'Moonlight'; //This can be used in the whole block  
let region = 'The Arctic'; //this sets region to arctic  
if (region === 'The Arctic') { //Opens a new block with if statment  
let lightWaves = 'Northern Lights';  
console.log(lightWaves); // returns 'Northern Lights'  
};
