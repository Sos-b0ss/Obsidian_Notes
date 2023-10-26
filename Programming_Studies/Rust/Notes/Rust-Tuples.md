When we need to group together data of differing types, we cannot use an array or Vec as they are homogenous collections. To create compound types with differing contained types, we can utilize the tuple 'primitive'. (See. https://www.codecademy.com/courses/rust-for-programmers/articles/primitives-rust)
\
**Tuple Declaration:**
\
We can declare a tuple by placing our data within parenthesis, '()'.
	ex:

	//Here we have a tuple of type (char, i32, str).
	let awesome = ('q', 38, "this is great");

We can access the fields of a tuple by tacking on a `.` and then providing the respective fields index. This is referred to as _dot notation_.
\
Like most programming languages, Rust uses 0-based indexing, which means that our first field is accessed with `.0`.
	ex:

	let cat = ("Meowzer", 10, true);

	let name = cat.0; // "Meowzer"
	let age = cat.1; // 10
	let awake = cat.2; // true

**Destructuring:**
\
We can destructure a tuple anywhere the Rust syntax allows it.
	ex:

	//This function will return our tuple.
	fn get_cat() -> (&'static str, f64, bool) {
		("Meowzer", 2.8, true)
	}

	// Destructuring within the variable assignment.
	let (name, cuteness, is_sleeping) = get_cat();
	println!("This is our cat {name}.");

	// We can ignore unused fields with `_`
	let (name, _, _) = get_cat();
	println!("This is our cat {name}.");

	// Destructuring within a match expression:
	match get_cat() {
		(name, _, is_sleeping) => {
			if is_sleeping {
				println!("{name} is sleeping.");
			} else {
				println!("{name} is awake");
			}
		}
	}
		// We can ignore a range of fields with `..`
		(name, ..) => {
			println!("{name} is cute when asleep or awake.");
		}
	}

**Tuple Struct:**
\
If we want to re-use a tuple across our codebase, we can define it as it's own custom type. This is referred to as a _Named Tuple_ or a  _Tuple Struct_.
\
To declare a Tuple Struct we utilize the 'struct' keyword. Here we have named our tuple struct 'Cat'.
	ex:

	// Tuple struct declarations must end with a ';'
	pub struct Cat(&'static str, f64, bool);

	// Now our type signatures are much shorter.
	fn get_cat() -> Cat {
		Cat("Meowzer", 2.8, true)
	}

The advantage of naming our tuple is that we can then create methods specific to this type utilizing an 'impl' block. (See. https://www.codecademy.com/courses/rust-for-programmers/articles/structs-rust)
\
**() Unit Type:**
\
A tuple that does not contain any fields, '()', is its own primitive type in Rust called the _unit_ type. We can think of the unit type as a piece of data, but without any actual data. It's only value is its own existence.
\
This type helps provide a safe way to handle certain situations while avoiding the pitfalls of a "null" type.
	ex:

	let this_variable_exists = ();

A function which does not return any value actually returns "()".
	ex:

	fn empty_function() {
		// A function without a return signature...
	}

	fn empty_expanded() -> () {
		// ... actually expands to this.
		// Both syntaxes are valid.
		()
	}

**Unit Structs:**
\
We can also give names to our own custom unit types. These are called "Unit Structs" and are useful when working with 'traits.' (See. https://www.codecademy.com/courses/rust-for-programmers/articles/traits-rust)
	ex:

	// We do not need to append `()` as it is inferred.
	pub struct NoValue;
