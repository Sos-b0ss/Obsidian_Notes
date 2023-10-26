Mutability is the capability of a variable's value to be altered in memory. In Rust, all variables are immutable by default.
\
This design decision is extremely useful in practice and helps us avoid unintended behavior.

**Mut:**

Immutability means that once a variable is declared with 'let', its value cannot change. To alter a value, we must explicitly declare it as mutable with the 'mut' keyword:
	ex:

	//Immutable
	let three = 3;

	//Mutable
	let mut any_number = 20;

Once we have declared a variable as mutable, we can reassign the value with the '=' operator:
	ex:

	let mut number = 20;

	//Reassign explicitly
	number = 22;

	//Increment and decrement
	number += 1;
	number -= 3;

While mutable states are sometimes the best approach to a particular problem, in Rust, it is general advised to avoid mutability when possible.
\
To change a variable's value without mutation, we can choose to shadow a variable instead.
	ex.

	let number = 10;
	let number = number + 10;

	println!("{num}"); // prints "20"

See [[Rust_Shadow]]

This allows us to avoid the complexity of mutability but at the cost of extra memory allocation.

**Mutable References:**

It is also possible to mutate values by reference with '&mut'.
	ex:

	fn question(s: &mut String) {
		s.pop();
		s.push('?');
	}

	let mut sentence = String::from("I am.");
	question(&mut sentance);

	println!("{sentence}");

We can only have one mutable reference to a piece of data at a time. This means we cannot immutably borrow a mutable reference outside the lifetime of the mutable reference.
	ex:

	let mut sentence = String::from("Take care, take care.");
	let immutable_reference = &mut sentence;

	//Swapping the order of these statements will cause the code to not compile.
	println!("{}", immutable_reference);
	println!("{}", sentence);

See: [[Rust_Lifetimes]]

**Interior Mutability:**

For more complex data types, we can only declare mutability on the entire type. All fields are either immutable or mutable.
	ex:

	struct Coordinate {
		x: i32,
		y: i32,
	}

	let mut coord = Coordinate { x: 20, y:20 };

	// We can mutate each field because coord is mutable.
	coord.x = 12;
	coord.y = 91;

Allowing mutability of a field when our data structure is otherwise immutable is called "Interior Mutability." Rust's std library provides us the 'std::cell::Cell' and 'std::cel::RefCell' types which allow this capability.

Be warned that these types can circumvent compile-time guarantees and generate runtime errors when not used properly. The std::cell documentation found here: https://doc.rust-lang.org/std/cell/index.html has more information about the implications.

