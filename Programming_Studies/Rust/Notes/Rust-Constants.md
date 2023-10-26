In Rust, constants are immutable data or functions that are declared at compile time.
\
When we have a piece of data that is used in many places throughout a codebase, we can avoid code duplication and ease development by utilizing constants.
\
**Const:**
We can declare a constant with the const keyword. Constant names must follow the SCREAMING_SNAKE_CASE convention.
\
Constants always require a type declaration and only types with a known size at compile time can be declared as a constant:
	ex:
	
	const ANIMAL: &str = "penguin";

	// string does not have a known size, so it cannot be used as a constant
	// The below commented code will not compile.
	// const OOPS: String = String::from("sorry");

Constants can be assigned to any expression as long as that expression can be computed at compile time.

	const SECONDS_IN_A_DAY: usize = 60 * 60 * 24;

Constants follow the same visibility requirements as any other expression.

	mod calculation {
		pub const REVOLUTIONS: usize = 38;
	}

	pub fn number_of_revolutions() {
		let revolutions = calculation::REVOLUTIONS;
		println!("{revolutions} revoltuions per second");
	}

**Const fn:**

In Rust, function pointers are a primitive data type. This means we can declare functions as constants. Making a function constant will enforce restrictions to validate that the function will provide the same result whether evaluated at compile time or runtime. This is similar to the concept of a mathematically "pure function" and helps to prevent unintended side effects.
\
const fn parameters are limited to datatypes with a known size at compile-time:
	ex:

	const fn days_to_seconds(days: usize) -> usize {
		days * 60 * 60 * 24
	}

	// We can utilize constant functions within other constant declarations
	const WEEK_IN_SECONDS: usize = days_to_seconds(28);

	println!("{WEEK_IN_SECONDS}");
	println!("{february_in_seconds}");

**Associated Constants:**

Rust also allows 'associated constants' which are constants declared within traits.
	ex:

	trait Golf {
		const BIRDIE: i32 = -1;
	}

	struct Caddy;

	impl Golf for Caddy {}

	println!("{}", Caddy::BIRDIE);

Constants are an ever-progressing aspect of the Rust language. Soon on the horizon, we can expect [[Rust_Constant_Generics]]