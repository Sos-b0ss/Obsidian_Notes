Sources:
https://www.udacity.com/blog/2021/07/cpp-dereferencing-explained.html
https://owasp.org/www-community/vulnerabilities/Null_Dereference
https://cwe.mitre.org/data/definitions/476.html
\
See. [[Pointer]]s
\
A [[Null-pointer]] dereference takes place when a [[Pointer]] with a value of NULL is used as though it pointed to a valid memory area. Null-pointer dereferences, while common, can generally be found and corrected in a simple way.
\
The * Operator in [[Pointer_Declaration]] vs. Dereferencing. The * operator can certainly make [[Pointer]]s and dereferencing confusing as there are two entirely different uses for the operator.. The first time we'll see the * operator in code is when we declare a specific variable as a pointer. Since we have to assign a data type to our pointers, we use the * operator at that time.
\
Once a variable is declared as a pointer, we no longer need to use the * operator when referring to the pointer in our code. The program will remember that the variable is declared as such. For the sake of code readability, it’s highly advised to name a pointer something that leaves no doubt as to its being a pointer.
\
But when using dereferencing, we need to call upon the _operator in a different way. With dereferencing, we need to use the_ operator whenever we want to reference the value of the variable that the pointer is pointing to.
