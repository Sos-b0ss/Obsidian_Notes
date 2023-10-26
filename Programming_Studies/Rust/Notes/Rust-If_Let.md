
When you want to compare against data within a complex type, Rust provides us with the 'if let' pattern. This allows you to destructure a type and access its inner value with a concise syntax.
\
**If let:**
The 'if let' pattern its best exemplified and most commonly encountered when accessing the values of 'monadic types' (See. https://www.codecademy.com/courses/rust-for-programmers/articles/monads-and-option) such as `Option<T>` and `Result<T, E>`.
	ex:

	let vault = Some("Whales are incredible!");

	if let Some(secret) = vault {
		println!("The secret is: {secret}");
	}

Here we are extracting the inner value of our `Option<T>` type by destructuring the 'vault' variable. This provides us with the new variable 'secret', which is the value contained inside our 'Some()' variant.
\
Without this pattern, we would have to 'unwrap()' the value to access the inner value when utilizing an 'if' expression. Here is how you would need to write the previous example with just an 'if' expression:
	ex:

	if vault.is_some() {
		println!("The secret is: {}", vault.unwrap());
	}

But since 'unwrap()' always has the capability of panicking, 'if let' is a much safer alternative to unwrapping.
\
Also, since 'matching' (See. https://www.codecademy.com/courses/rust-for-programmers/articles/match-rust) allows destructuring, we can write the same 'if let' statement as a 'match'.
	ex:

	match vault {
		Some(secret) => println!("The secret is: {secret}"),
		_=> {}
	}

**Declaring Variables:**

It is helpful to remember that since 'if let' is an expression, it can be used to conditionally declare a variable.
	ex.

	let whale_name = Some("Herby");

	let has_a_name = if let Some(name) = whale_name {
		println!("Ahoy, {name}");
		true
	} else {
		false
	};

Just like 'if', 'if let' must be fully exhaustive. This means when our conditional block is an expression, we must provide an 'else' block that returns the same type.

**Destructing Other Types:**

While 'if let' is commonly seen on monadic types, we can utilize it on any data type which can be destructured.
\
**Tuples:**
	ex:

	let whale = ("Ahab", "Humpback");

	if let ("Ahab", species) = whale {
		println!("Funny name for a {species} whale");
	}

	// We can use '_' to ignore a specific field while matching.
	if let ("Tony", _) = whale {
		println!("Say hello to Tony the whale!");
	}

**Enums:**
	ex:

	enum Fish {
		Carp,
		Flounder,
		Coy(String)
	}

	let my_pet = Fish::Coy("Wanda".to_string());

	if let Fish::Flounder = my_pet {
		println!("Meet my pet flounder.")
	}

	if let Fish::Coy(name) = my_pet {
		println!("My pet's name is {name}");
	}

**Structs:**
	ex:
	
	struct Ocean {
	name: &'static str,
	inhabitants: u64,
	}

	let ocean = Ocean {
		name: "Pacific",
		inhabitants: 722882038408,
	};

	if let Ocean { name: "Atlantic", inhabitants: i } = ocean {
	}

	// The special operator '..' can be used to ignore all remaining fields when matching on a complex data structure.
	if let Ocean { name: "Pacific", .. } = ocean {
		println!("We are in the Pacific Ocean");
	}

