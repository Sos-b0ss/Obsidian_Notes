A computer program is fundamentally made up of two things: data and instructions for manipulating that data. These instructions are called **functions** and are the things that make our code work.
\
**Function Declarations:**
\
You can declare a function in Rust with the 'fn' keyword. Declaring a function requires supplying a name for the function, any potential parameters, and a block for the body of the function:
	ex:

	// Declaring a function
	fn say_howdy() {
		println!("Howdy!");
	}

	// Calling a function
	say_howdy();

Function bodies have their own 'scope' and cannot access variables from the local environment. (See. https://www.codecademy.com/courses/rust-for-programmers/articles/scope-and-ownership)

	let out_of_scope = "sorry, this won't compile";

	fn my_function() {
		// This will not compile.
		// println!("{out_of_scope}");

		let in_scope = "this will compile";
		println!("{in_scope}");
	}

If you need to access variables from the local environment, closures are a kind of lazy function that allow this. (See. https://www.codecademy.com/courses/rust-for-programmers/articles/closures)
\
**Return Values:**
\
We can specify a return value for a function with the -> operator followed by the returned type. This is placed after the function name and before the function's block.

	//Here were returning a 'i32'
	fn another_function() -> i32 {
		27
	}

	// Assigning a returned value to a variable.
	let integer = another_function();

	println!("{integer}"); // This will print "27".

**Parameters:**
\
Functions can take data as inputs to operate on. These are called 'input parameters' and in Rust, parameters always require a type signature.
\
Type signatures are declared with the parameter name, followed by a `:`, followed by the type. Multiple parameters are separated by a `,`.
\
This 'multiply' function takes two arguments of type u32 and multiplies them together:
	ex:

	fn multiply(first: u32, second: u32) -> u32 {
		first * second
	}

Since all parameters for a function must be manually declared and of a specified type, variadic functions do not exist in Rust. However, we can use 'macros' to mimic this behavior.
\
The 'format!()' macro in Rust's std library is a great example of this. (See. https://www.codecademy.com/courses/rust-for-programmers/articles/macros-rust)
\
**Functions as Parameters:**
\
You can also pass functions as parameters with the 'fn' pointer primitive. The type signature for a 'fn' parameter requires type annotations and takes the form 'fn(T) -> T'.
\
Here the call to the 'roundabout' function will call the function we pass to it.
	ex:

	fn increment(num: u32) -> u32 {
		num + 1
	}

	fn decrement(num: u32) -> u32 {
		num - 1
	}

	fn roundabout(f: fn(u32) -> u32, num: u32) -> u32 {
		f(num)
	}

	let inc = roundabout(increment, 2); // This returns 3
	let dec = roundabout(decrement, 2); // This returns 1

Note that when we are passing as function pointer as an argument, we forego the trailing ().
