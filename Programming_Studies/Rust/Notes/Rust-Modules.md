Once a codebase gets large, it becomes helpful to seperate our code into distinct sections. Rust has a module system that provides user-defined namespacing within the codebase.
\
**Mod:**

You can define a module using the 'mod' keyword. A module has its own distinct scope and visibility.
\
Here there's a defined module named 'cake' with an 'is_favorite()' function inside of it:
	ex:

	mod cake {
		pub fn is_favorite(name: &str) -> bool {
			name == "Coconut"
		}
	}

Once a module has been declared, its content can be accessed by utilizing 'path syntax.' A 'path' is created by chaining any number of nested modules together with the :: operator.
\
Now, to utilize the 'is_favorite()' function by accessing it by its path.
	ex:

	let guess = cake::is_favorite("Marble");

Utilizing paths intentionally in our code is one way of increasing our code's readability.
\
**Nesting Modules:**

Modules can be nested indefinitely:
	ex:

	mod cake {
		pub mod flavors {
			pub const COCONUT: &str = "Coconut";

			pub mod toppings {
				pub const SPRINKLES: &str = "Sprinkles";
			}
		}
	}

	println!("{}", cake::flavors::COCONUT);
	println!("{}", cake::flavors::toppings::SPRINKLES);

**Importing Items:**

You can import any module or contained item into the current scope with the 'use' keyword followed by the path to the item you wish to import.
\
The item being imported must be declared as public with the 'pub' keyword. All items in Rust are private by default.
	ex:

	mod cake {
		pub mod flavors {
			pub const COCONUT: &str = "Coconut";
		}
	}

	// A module must be 'pub' to access it by name.
	use cake::flavors;

	println!("{}", flavors::COCONUT);

**Exporting Items:**

When out crate is a library, making an item public with 'pub' will expose that item to users of our library. Rust also allows us to limit where an item is accessible when we make it public.
\
If we have a function that we want to make public internally within the crate but not to users of the library, then you can use 'pub(crate):'
	ex:

	pub(crate) fn print_lemon() -> {
		println!("Lemon");
	}

The public nature of this item now only extends to the crate it is defined in. Other designations include the parent module, with 'pub(super)', or we can designate a specific module with the 'in' keyword, 'pub(in path::to::module)'.

**Seperate Files:**

Once a single file is not sufficient for holding all the code, you can move modules into their own separate files. When we add a source file to our crate's 'src/' directory, we can treat that file's contents as a module that can be imported.
\
To put the 'cake' module into a separate file, you would:
\
1. Create the file src/cake.rs and move the code into it.
2. Define the file as a module by adding 'mod cake;' to the main.rs file.

	mod cake;

	fn main() {
		let guess = "Lady Baltimore";

		if cake::is_favorite(guess) {
			printlin!("That's my favorite cake!");
		} else (
			println!("Not my favorite, but still delicious.");
		)
	}

When using separate files, we can nest the files within folders that have the same name as the module:

	src/
	|--main.rs
	|--colors.rs
	|--colors/
		|--hex.rs

A file with the name mod.rs within a module's folder can take the place of a named file:

	src/
	|--main.rs
	|--colors/
		|--mod.rs
		|--hex.rs

**Crate::,super::,self::**

When you need to access a module that is not a direct child of the current module, Rust provides us with keywords to quickly navigate the module tree.

- To access modules from the root of the project, you can use crate::.
- To access the relative parent module, you can use super::.
- To access the current module, you can use self::.


		// Inside the main.rs file:
		pub const FLOUNDER: &'static str = "flounder";

		fn main() {
			mod ocean {
				pub const ATLANTIC: &'static str = "Atlantic";

				mod fish {
				fn print_flounder() {
					use crate::FLOUNDER;
					use super::ATLANTIC;

					println!("A {FLOUNDER} in the {ATLANTIC}")
					}
				}
			}
		}

**External Crates:**

After adding a dependency to the 'Cargo.toml', you can import it by name:

	// Here we are importing the external 'rand' crate
	use rand;

	let random_bool = rand::random();

**Renaming Imports:**

We can also rename any import within our codebase with the 'as' keyword. This is useful for naming conflicts and making the code more readable.

	use i32 as Integer;

	let number: Integer = 137;

