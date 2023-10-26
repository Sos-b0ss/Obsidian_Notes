To best understand closures, let's take a look at their most verbose form. Closures follow a very similar syntax to functions but with input parameters placed between '||'.
\
Here we have declared a function that squares an integer and a closure that accomplishes a same task.
	ex:

	// Function
	fn square_function(a: i32) -> i32 { a * a }

	// Closure
	let square_closure = |a: i32| -> i32 { a * a };

We rarely see closures in this verbose form thanks to Rust's ability to infer parameter and return types. Additionally, the body of a closure does not require '{}' braces.
	ex:

	// Single argument
	let square = |a| a * a;

	// Multiple arguments are separated by a comma
	let multiply = |a, a| a * b;

	// No arguments
	let hundred = || 10 * 10;

When we store a closure as a variable, we can call it the same we would a function.
	ex:

	square(5);
	multiply(5, 10);
	hundred();

**Capturing Environment:**
\
Closures differ from functions in that they can capture values from the scope they are defined in. Here we are utilizing the 'house_number' variable directly within out 'where_are_we' closure.
	ex:

	let house_number = 388;
	let where_are_we = || println!("{house_number}");

	where_are_we();

When we capture values from the environment, they are taken by reference.
\
**Ownership and move:**
\
We can tell a closure to take 'ownership' of the local data it utilizes by placing the 'move' keyword in front our closure declaration. (See. https://www.codecademy.com/courses/rust-for-programmers/articles/scope-and-ownership)
	ex:

	let answer = 928;

	//Here we have moved the data from 'answer' into the 'is_correct' closure
	let is_correct = move |x| x == answer;

	// We can no longer access 'answer', but we can now use our closure to validate we have the correct answer.
	println!("{}"", is_correct(23)); // false
	println!("{}", is_correct(928)); // true

**Closures as Data Structures:**
\
We talked previously in the functions article about how function pointers are a primitive datatype. Since closures are also functions, we can use them as fields in structs or tuples.
(See. https://www.codecademy.com/courses/rust-for-programmers/articles/functions-rust)
	ex:

	struct Magic {
		field: fn(),
	}

	let almost = Magic {
		field: || println!("almost magic!"),
	};

We can get even more specific in regards to ownership and mutability by utilizing generics with the 'Fn', 'FnMut', and 'FnOnce' traits.
\
**Laziness:**
\
Closures in Rust are lazy, which means that they are not computed until called. When we have a function that takes a long time to compute, we can often achieve performance in our program by rewriting our function as a closure.
\
A good example of the effects of laziness can be found in the 'Functional Iteration' article. (See. https://www.codecademy.com/courses/rust-for-programmers/articles/functional-iteration)
