~ reusable pieces of code that can be exported from one program and imported to another  
  
~ This is incredibly useful for a number of reasons..  
Using MODULES you can:  
- find, fix, and debug more easily  
- reuse, and recycle defined logic in different parts of the application  
- Prevent pollution of the global namespace and potential harming collisions by cautiously selecting variables and behaviour we load into a program.  
  
~ How to prime and define a module using ".exports"  
ex: let Menu = {};  
Menu.Specialty = "baby carrots";  
module.exports = Menu;  
(see how the pattern used to define a module is:  
- Define and object to represent the module.  
- Add data or behaviour to the module.  
- Export the module)  
  
~To make use of an exported module we use the "require()" function.