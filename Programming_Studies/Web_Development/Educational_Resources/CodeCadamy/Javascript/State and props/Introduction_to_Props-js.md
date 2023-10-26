~A component can pass information to another component.  
Information that gets passed from one component to another is known as "props."  
  \
~You can pass information to a React component by giving that component an attribute  
ex:  
\
"<"MyComponent foo="bar" />  
\
~To pass information to a component, you need a name for the information that you want to pass.  
ex:  
\
"<"Example message="This is some top secret info." />  
~In the above example, we used the name message. You can use any name you want.  
  \
~To pass information that isn't a string, wrap the information in curly braces.  
ex of an aray:  
\
"<"Greeting myInfo={["top", "secret", "lol"]} />  
ex of multiple forms of info being passed:  
(anything that isnt a string is in a pair of {})  
"<"Greeting name="Frarthur" town="Flundon" age={2} haunted={false} />  
  \
~When you need a component to display the information that you pass use these steps:  
1 - Find the component class that is going to receive that information.  
2 - Include this.props.name-of-information in that component class's render method's return statement.
