~New method syntax:  
(doesnt require arrow syntax or a colon (:) with the function keyword  
\
ex:  
so it turns the prev ex of:  
openRestaurant: () => {  
return 'walk in and die on the inside'  
};  
\
NOW:  
openRestaurant() {  
return 'nice, now I can write less clutter!'  
};  
\
~This keyword:  
When a var or key you try to referance is not in the scope you can use '.this' to properly refer to it.  
\
ex:  
const restaurant = {  
name: 'you know',  
hasDineInSpecial: true,  
openRestaurant() {  
if (hasDineInSpecial) { //gotta put this. to fix write (this.hasDineInSpecial)  
return 'Ooo. Ouch.. this hurts my computer brain'  
} else {  
return 'please use \'this.\' because then it will let me know the scope is in \'this.\' object, thx!'}
