!With Rust, a variable is an identifier that points to a location in memory. This location in memory can be either data or a function.
\
**Variable Declarations**
To assign variables in Rust we utilize the 'let' keyword with the = operator taking the following form:
	ex:

	let variable = "this is a &str";

We can assign variables to any expression:
	ex:

	\\ This is a closure
	let double = |d| d * 2;

	\\ This is the outcome of calling the closure
	let var = double(10);

**Inferred Types**

The Rust compiler is good at inferring types based on context. In the following example, the datatype of 'stars' is inferred from the function 'double()'s input parameter signature.
	ex:
	fn double(num: u128) -> u128 {
		num * 2
	}

	let stars = 10; // This is of type 'u128'

When there is no context for primitive types, Rust will fall back to 'i32' for untyped integer literals and 'f64' for untyped floating point literals.
	ex:
	
		let integer = 10; // This is of type 'i32'
		let float = 1.2; //This is of type 'f64'

**Type Signature**
We can manually annotate types by providing a type signature. Type signatures are declared with ': Type' placed after the variable name and before the assigning '=:'
	ex:

		let small_integer: u16 = 28;

		fn double(num: u128) -> u128 {
			num * 2
		}

		let unsigned_int: u8 = 28;

**Shadowing:**
We can assign a new value to the same variable name within the same scope. This is called shadowing and does not alter the original assignment:
	ex:

		let favorite = "orange";
		println!("{favorite}");

		let favorite = "cerulean";
		Println!("{favorite}");

		let favorite = "yellow";
		Println!("{favorite}");

Shadowing a variable will always allocate memory for the new variable.

**Pattern Binding:**
'Let' statements accept a pattern on the left-hand side of the '=' operator. This means we can bind multiple variables in a single 'let' statement using a tuple:
	ex:

		let (a, a) = (10, "pie");

We can also construct an array while declaring variables for each member:
	ex:

		let [noun, verb, adjective] = ["arrays", "are", "homogeneous"];

**Unused Variables:**
The Rust compiler will give us warnings anytime we have unused variables. We can tell the compiler to not check this requirement by prefixing a variable name with '_:'
	ex:

		fn no_warnings() {
		let _unused = "never";
		let _used = "sometimes";
		
		println!("{_used}");
		}
