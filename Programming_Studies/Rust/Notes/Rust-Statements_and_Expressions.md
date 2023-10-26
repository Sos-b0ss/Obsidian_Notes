**Statements:**
\
A segment of code that doesnt return any value. Like:

```
// This is a statement, but we cannot access its value
"purple";
```

If you use 'let' keyword to hold a piece of data its called a 'let statment', as it holds the data but does not return the value itself:

```
// We can access the data created by this statement with the variable answer
let answer = "purple";
```

A function or macro the does not return any data is also a statement:

```
fn say_answer() {
	let answer = "purple";
	println!("{answer}")
}
```

The previous example doesnt require a ';' on the last line of the function body because println! is also a statement.
\
**Expressions:**
\
An expression is a segment of code that returns a value. Since Rust is an 'Expression-oriented' language, all code blocks will implicity return their value unless we utilize a semicolon to terminate the expression:

```
// This is an expression, it will return the &str "green"
"green"
```

A function or macro that returns a value is also an expression:
```
fn give_answer() -> String {
	let answer = "green".to_string();
	answer
}
 
println!("{}", give_answer());
```

**Patterns:**
Rust's syntax also allows Patterns, which are special syntax rules that can be used in certain situations. Patterns help to make the language more readable and allow us to do things that are otherwise not easily accomplished.
\
One example of a pattern is the ability to declare multiple variables within the same let statement:

```
let (x, y) = (5, 10);
```

Theres many other patterns availabel that have their own special syntactical rules.
\
A comprehensive list of patterns can be found in the 'Rust Reference." here:
https://doc.rust-lang.org/reference/patterns.html#identifier-patterns
