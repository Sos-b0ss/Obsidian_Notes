-A component can do more than just read its own state. A component can also change its own state. Do this by calling the function: this.setState()  
  \
-this.setState() takes two arguments: an object that will update the component's state, and a callback. You basically never need the callback.  
  \
-this.setState() takes an object, and merges that object with the component's current state. If there are properties in the current state that aren't part of that object, then those properties remain how they were.