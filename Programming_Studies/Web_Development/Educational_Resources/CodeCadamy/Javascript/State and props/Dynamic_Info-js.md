-React components will often need dynamic information in order to render.  
  \
-There are two ways for a component to get dynamic information: props and state. Besides props and state, every value used in a component should always stay exactly the same.  
  \
-props and state are all that you need to set up an ecosystem of interacting React components.  
  \
-Unlike props, a component's state is not passed in from the outside. A component decides its own state.  
  \
~To make a component have state, give the component a state property. This property should be declared inside of a constructor method, like this:  
  \
class Example extends React.Component {  
constructor(props) {  
super(props);  
this.state = { mood: 'decent' };  
}  
  \
render() {  
return <div></div>;  
}  
}  
  
<Example />  
  
-this.state should be equal to an object  
  
-to learn more about the ES6 syntax such as the "constructor" and "super" read up: 
[https://hacks.mozilla.org/2015/07/es6-in-depth-classes/](https://hacks.mozilla.org/2015/07/es6-in-depth-classes/)  

---
-It is important to note that React components always have to call super in their constructors to be set up properly.  

---
-Make sure not to separate constructor and render with a comma! Methods should never be comma-separated, if inside of a class body. This is to emphasize the fact that classes and object literals are different.
