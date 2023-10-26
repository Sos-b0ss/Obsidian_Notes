Controlling the flow of the Rust code is an important aspect of any programming language. While Rust has mutliple ways of accomplishing this, the most basic approach is through the use of 'if' and 'else'.
\
**If/else:**
You can conditionally execute blocks of code based on the outcome of any boolean expression by utilizing the 'if' keyword. To handle the remaining cases, we can use the 'else' keyword:
	ex:

	let is_daytime = true;

	let is_daytime {
		println!("What a beautiful day!")
	} else {
		println!("Zzzzzzzzzzzzzzzzzzzzz")
	}

**Else if:**

You can use 'else if' to provide additional conditional checks.
	ex:

	#[derive(PartialEq, Eq)]
	enum Flower {
		Lilac,
		Orchid,
		Daffodil,
	}

	let flower = Flower::Daffodil;

	if flower == Flower::Lilac {
		println!("a lilac");
	} else if flower == Flower::Orchid {
		println!("a beautiful orchid");
	} else {
		println!("another flower");
	}

**Exhaustiveness:**

Rust's conditional evaluations are fully exhaustive, so every possible outcome must be accounted for. This means that when an 'if' block is an expression, every 'else if' and 'else' block must return the same type:
	ex:

	let carrots = 12;

	let rabbit_status = if carrots > 10 {
		"in burrow"
	} else if carrots == 9 {
		"snagging one more carrot"
	} else {
		"on the prowl"
	};

	println!("{rabbit_status}");

We do not need to provide an 'else' keyword when our conditional block is a statement because statements inherently return the unit type (See. https://www.codecademy.com/courses/rust-for-programmers/articles/tuples-rust), '()'.
	ex.

	if true {
		println!("this is shorthand");
	}

	if true {
		println!("for this...");
		()
	} else {
		()
	}

**Conditional Operators:**

Rust provides us with operators for conditional evaluations. These operators can be used on any type that implements the respective traits found in Rust's standard library.

**Equality:**

Equality can be checked with `==` and and non-equality with `!=`
\
These operators will work on any type which implements the 'Eq' or 'PartialEq' traits. (See. https://doc.rust-lang.org/std/cmp/trait.Eq.html, & https://doc.rust-lang.org/std/cmp/trait.PartialEq.html)
	ex:
	let track_number = 8;

	if track_number == 9 {
		println!("number nine");
	}

	if track_number != 9 {
		println!("flip the record");
	}

**Ordering:**

Ordering on a type can be compared with '<', '>', '<=', '>='.
\
These operators will work on any type which implements the 'Ord' or 'PartialOrd' traits. (See. https://doc.rust-lang.org/std/cmp/trait.Ord.html, & https://doc.rust-lang.org/std/cmp/trait.PartialOrd.html)
	ex:

	let pancakes = 10;

	if pancakes < 3 {
		println!("Eat more pancakes.")
	} else if pancakes > 10 {
		println!("Uh oh...")
	} else if pancakes == 10 {
		println!("That's a lot of pancakes")
	} else {
		println!("Mmm syrup")
	}

Keep in mind that since equality and ordering are handled by their respective traits, we can implement conditional operators for our own custom data types.
