ex code:  
const visibleLightWaves = ( ) => {  
let visibleLightWaves = 'Moonlight'; //This can be used in the whole block  
let region = 'The Arctic'; //this sets region to arctic  
if (region === 'The Arctic') { //Opens a new block with if statment  
let lightWaves = 'Northern Lights';  
console.log(lightWaves); // returns 'Northern Lights'  
};  
  \
~so when the example code is ran it displays:  
Northern Lights  
Moon Lights  
  \
-even though lightwaves was set to different strings it was declared in a block and therefore separate from each other.  
  \
~ Use in a for loop:  
\
const cloudCount = ( ) => {  
let i = 2; //2 is set to var i  
for (let i = 0; i < 10; i++;) {//sets i to 0  
console.log(i) //runs through all the # 0 to 9  
}  
};  
\
CloudCount(); //runs the function returning both 2 and 0,1,2,3,4,5,6,7,8,9  
  \
console.log(i); //returns undefined because globally i is not set to anything.
