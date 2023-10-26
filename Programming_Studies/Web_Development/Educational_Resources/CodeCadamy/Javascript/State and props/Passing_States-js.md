-When Calling "this.setState" from another function:  
  
-The most common way to call this.setState() is to call a custom function that wraps a this.setState() call. .makeSomeFog() is an example:  
  
class Example extends React.Component {  
constructor(props) {  
super(props);  
this.state = { weather: 'sunny' };  
this.makeSomeFog = this.makeSomeFog.bind(this);  
}  
  
makeSomeFog() {  
this.setState({  
weather: 'foggy'  
});  
}  
  
-This concept can get pretty tricky read this thoroughly: [https://reactjs.org/docs/handling-events.html](https://reactjs.org/docs/handling-events.html)
