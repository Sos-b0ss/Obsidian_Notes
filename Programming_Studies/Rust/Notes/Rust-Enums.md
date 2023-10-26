When we need a data type whose value can be only one of a set number of variants, Rust provides us with "Enumerations."
\
**Enum Declaration:**
\
To create an _enumeration_, often just called an _enum_, we utilize the 'enum' keyword. Every variant for our enum is placed within its declaration block. Variants follow the "PascalCase" naming convention.
	ex:

	enum InnerPlanet {
		Mercury,
		Venus,
		Earth,
		Mars,
	}

Now that we have declared our enum, we can create a value of a specific variant using the '::' operator.
	ex:

	let home = InnerPlanet::Earth;

**Matching:**
Since an enum's value can only be a single variant, 'matching' on an enum is a very common and useful programming pattern in Rust.
	ex:

	let vacation_location = InnerPlanet::Murcury;

	match vacation_location {
		InnerPlanet::Murcury => println!("Bring sun protection"),
		InnerPlanet::Venus => println!("Quire blue."),
		InnerPlanet::Earch => println!("Lots to see here."),
		InnerPlanet::Mars => {
			println!("Brrr...");
			println!("Bring a coat!");
		}
	}

When matching on an enum, all variants must be handled. If we remove one of the match arms in the previous examples, our code will not compile.
\
We can use the `_` catch-all operator to handle the remaining unspecified variants.
	ex:

	match vacation_location {
		InnerPlanet::Earth => println!("Lots to see here."),
		_ => println!("Lets clean up Earth first..."),
	}

**Variant values:**
Enums variants can also contain values. This is possible enum variants in Rust are actually 'structs'. (See. https://www.codecademy.com/courses/rust-for-programmers/articles/structs-rust)
	ex:

	enum Meal {
		Pasta, // Unit struct
		StirFry(Vec<String>), // Tuple struct
		Burrito { // Struct with named fields
			beans: bool,
			rice: bool,
		},
	}

We can access a variant's inner data by destructuring.
	ex:

	let dinner = Meal::Burrito {
		beans: true,
		rice: false,
	};

	match dinner {
		Meal::Pasta => println!("Too heavy."),
		Meal::StirFry(veggies) => {
			println!("{veggies:?}")
		}
		Meal::Burrito { beans, rice } => {
			println!("with beans: {beans}");
			println!("with rice: {rice}")
		}
	}

**Impl Blocks:**
\
Like structs, enums are our own custom data type. We can provide methods for our enums through an 'impl' block.
	ex:

	enum Determination {
		Yes,
		No,
		Potentially,
	}

	impl Determination {
		pub fn totally() -> Self {
			Self::Yes
		}
	}

