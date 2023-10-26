When you have predetermined what you want every variable possibility to do you can use else if statements. Like ternary statements they will only push if the conditions are not met, however rather than be only used for truthy it can be utilized for much more.  
ex:  
let runnerAge = 19;  
let runnerEarly = true;  
if (runnerAge > 18 && runnerEarly) {  
console.log('I am early, and over 18/yo);  
} if else (runnerAge > 18, !runnerEarly) {  
console.log('I am late to register, but over 18/yo');  
} if else (runnerAge < 18, !runnerEarly) {  
console.log('I am under 18/yo and late, figures');  
} else {  
console.log('please register at front desk!');  
}  
  
	~ You can see that in this else if statement it takes 3 different conditions and logs what you want each condition to be equal to. If they're 18/yo or older and early then it logs that, 18/yo or older and late it logs that, etc. It even logs if none of the conditions are met.

