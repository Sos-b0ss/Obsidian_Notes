~How to define an eventhandler in react:  
You define an event handler as a method on the component class, just like the render method. Almost all functions that you define in React will be defined in this way, as methods in a class.  
  \
ex:  
import React from 'react';  
  
class Example extends React.Component {  
handleEvent() {  
alert(`I am an event handler.  
If you see this message,  
then I have been called.`);  
}  
  
render() {  
return (  
<h1 onClick={this.handleEvent}>  
Hello world  
</h1>  
);  
}  
}
