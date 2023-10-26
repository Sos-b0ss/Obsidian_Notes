~ Say you make a cat class and its just about identical to the dog one execpt it requires a few new properties you can use inheritance to cut down ont he amount of code you have to write.  
~Using inheritance you can create a parant class or a 'SupperClass' with properties and methods that multiple child or 'SubClasses' can share.  
~ Simple enough, child classes inherit methods & properties from the parent classes. wonder how they got the name inheritence!  
  
ex flow chart:  
________________________________  
| Animal: |  
| Properties: name, behaviour |  
| Methods: .incrementBehaviour() |  
|_______________________________|  
| |  
| \  
| \  
________|_____________ _______\_________________  
| Dog: | | Cat: |  
| Properties: | | Properties: |  
| name, behaviour | | name, behaviour, usesLiter |  
| Methods: | | Methods: |  
| .incrementBehaviour() | | .incrementBehaviour() |  
|_____________________| |_________________________|  
  
~ See how the properties and methods between dog & cats both seem to inherit 'name, 'behaviour' as well as the method.  
(I'd guess cats and dogs are animals huh)

---

~ You write up a parent class the same way you do any other class:  
ex:  
class Animal {  
constructor (name) {  
this._name = name;  
this._behaviour = 0;  
}  
// make some getters here  
}  
  
~ How to extend an inhertance to a child class:  
ex: class Cat extends Animals {  
constructor (name, usesLitter) {  
super(name);  
this._usesLitter = usesLitter;  
}  
}  
~notice the new keywords 'extends' & 'super'  
-Extends: makes the methods of the parent available to the child  
-Super: calls the constructor of the parent class *ALWAYS call 'super' on the first line of subclass constructors*