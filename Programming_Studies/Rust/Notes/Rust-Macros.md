Rust's macro system is a way of manipulating and generating source code.
Macros allow you to do things that would otherwise not be possible in the normal language structure or require a large amount of code repetition.

**What are macros?:**

Macros are procedures that expand and generate raw source code before the 'rustc' compiler begins its compilation step. You can spot macros in a Rust program in two different places:
	ex:

	// Attributes are macros.
	#[derive(Debug)]
	struct Wow;

	let wow = Wow;

	// Calls ending with '!' are macros
	println!("{wow:?} that is convenient!");

In this example, the #[derive()] macro generate all the source code necessary for 'Wow' to be able to print debug out. The 'println!()' macro allows us to format and print a string with a convenient interpolation syntax.
\
Macros are a core part of the Rust language and can be very powerful tools for creating intuitive programmer interfaces for your library.
\
**Function-like Macros:**

Function-like macros look like normal function calls whos name ends with a '!'. One of the most commonly used macros in Rust is 'println!()' which prints a line of text to stdout.
	ex:

	let warm = "auburn";
	let cool = "cerulean";

	println!("the sky is {cool} and {warm}");

You may notice that we are using a special syntax to interpolate our variables.
\
Unlike functions, the input of the body of a macro call is arbitrary. The macro author has complete control over the syntactical bits of the language down to individual tokens.
\
When calling function-like macros, we can denote the body of the macro with (), [], or {} interchangeably.
 ex:

	// Macros utilizing '[]' are conventionally used for collections.
	let clouds = vec![12, 97, 24];

	//'rustfmt' will not format macros that utilize '{}'
	let today = println! {
		"look up
		toward the sky,
		it's a beautiful day."
	};

**'std' Library Macros:**

Macros are used very commonly throughout the std library. Let's take a peek at some of the most commonly used function-like macros.
\
'format!()'
\
We can interpolate and format strings with the 'format!()' macro.
	ex:

	let exit = 8;
	let town = "Willoughby";

	let address = format!("Next stop, {town}. Train is at exit number {exit}.");

The possibilities for interpolating and formatting values with this syntax are expansive. A detailed list of all capabilities can be found in the std::fmt documentation.
\
**Println!():**

'println!()' and 'print!()' internally call the 'format!()' macro while also printing the formatted String to stdout. Printing the stderr is accomplished with 'eprint!()' and 'eprintln!()'.

	let jungle_bird = "Macaw";
	let sound = "caws";

	print!("The {jungle_bird}"); // Does not print a newline
	println!(" {sound}.");       // Prints a newline

**Assert!():**

We can assert a conditional evaluation or panic upon failure with the 'assert!()' and 'assert_eq!()' macros. To assert non-equality, we can use 'assert_ne!()'.
	ex:

	let number = 12;
	let you = "us";
	let i = "us";

	assert!(you == i);
	assert_eq!(i, you);
	assert_ne!(number, you.len());

**Panicking Macros:**

We can utilize the 'unreachable!()' macro in situations where the compiler cannot determine code to be unreachable. The 'unimplemented!()' macro denotes that a part of your code has not yet been implemented. The 'todo!()' macro denotes the same but implies an intent to complete it.
\
These three macros will all panic if they are reached. We can also intentionally panic our program utilizing the 'panic!()' macro.
\
All of these macros can also optionally print a supplied string as a message upon panicking.
	ex:

	let number = 10;

	if number <= 5 {
		todo!("we will handle this outcome soon.")
	} else if number > 5 {
		unimplemented!("we might do something here eventually")
	} else {
		unreachable!()
	}
	panic!("we should use panics sparingly.");

**Attributes:**
The other place we commonly encounter macros in Rust is in the form of Attributes. These allow us to auto-generate code for certain types or to provide additional functionality.
	ex.

	// A commonly encoutered attribute.
	#[derive(debug)]
	struct Chapter(String);

More info about attributes and the #[derive()] macro can be found in this attributes article: https://www.codecademy.com/courses/rust-for-programmers/articles/attributes-rust

