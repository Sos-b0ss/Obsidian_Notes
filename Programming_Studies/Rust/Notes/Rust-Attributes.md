Attributes in Rust are macros that allow us to do special things with the language such as set compilation options, conditionally compile pieces of code, ignore lints, and denote tests and benchmarks.
\
Attributes can be declared inside the scope of the item it is being applied to, known as 'inner attributes', or before the item it is being applied to, known as 'outer attributes'.
\
**Inner Attributes:**

You can declare an inner attribute with #![attribute] placed as the first item declared in its scope. Inner attributes can be used in external blocks, functions, implementations, and modules.
\
You can forgo all compiler warnings throughout the entire codebase during development by placing #![allow(warnings)] at the top of the main.rs file:
	ex:

	//Inner attributes must be declared before any other items.
	#![allow(warnings)]

	fn main() {
		let unused_variable = "no warnings here";
	}

In this example, if you had placed the attribute at the top of a specific module file rather than the main.rs file, the attribute would only apply to that module and all child items.
	ex:

	fn no_warnings() {
		#![allow(warnings)]
		let unused_variable = "no warnings here";
	}

**Outer Attributes:**

You can declare an outer attribute on any item by placing '#[attribute]' before the item you would like it applied to.
\
These are some commonly encountered attributes:
	ex:

	//Defining a test.
	#[test]
	pub fn is_tru() {
		assert(trus, "successful test")
	}

	// Providing a deprecation warning for users of the library.
	#[deprecated(since = "0.2.0", note = "replaced by `is_true`")]
	pub fn isnt_not_true() {
		println!("The compiler will warn when using this function.")
	}

	// Optional complication based on target architecture.
	#[cfg(target_os = "linux")]
	pub fn distro_name(name: &str) {
		println!("your linux distrobution is: {name}");
	}

**Attribute Syntax:**

You may have noticed that the attributes we have seen so far have different syntaxes within their brackets. Here's some common input patterns you'll find in attribute macros:
	ex:

	//Named
	#[no_std]

	// Named with value.
	#[must_use = "This function should be used."]

	// Named with list of identifiers or paths.
	#[forbid(unsafe, warnings)]

	//Named with list of key values.
	#[cfg_attr(target_os = "linux", path = "os/linux.rs")]

**Derive:**

The most commonly encountered attribute used in Rust is the #[derive(trait)] attribute which allows us to automatically implement a trait for a type.
\
Here we can derive the 'Debug' and 'Clone' trait on our 'Chair' struct because its field's types, 'u32' and 'bool', already implement them.
	ex:

	#[derive(Debug, Clone)]
	struct Chair {
		legs: u32,
		wooden: bool,
	}

	let chair = Chair {
		legs: 4,
		wooden: true,
	}

	// Now we can print the debug output of our `Chair` type:
	println!("{chair:#?}")

'Debug' (See. https://doc.rust-lang.org/std/fmt/trait.Debug.html) is an extremely useful trait for development purposes. Other useful traits from the std library to derive include:
- 'PartialEq,' (See. https://doc.rust-lang.org/std/cmp/trait.PartialEq.html)
- 'Eq,' (See. https://doc.rust-lang.org/std/cmp/trait.Eq.html)
- 'Copy,' (See. https://doc.rust-lang.org/std/marker/trait.Copy.html)
- 'Clone,' (See. https://doc.rust-lang.org/std/clone/trait.Clone.html)

**Available Attributes:**

There are too many attributes built into the language to be able to dicuss them all. A comprehensive list can be found here: https://doc.rust-lang.org/reference/attributes.html
\
remember since attributes are procedural macros, we are not limited to the ones provided by the language. You can use 'procedural macros' created by others and even make your own. (See. https://www.codecademy.com/courses/rust-for-programmers/articles/procedural-macros-rust)
\
For inspiration on how useful macros can be to the quality of life of programmers, here is an example of a procedural macro from the 'rocket' crate. (See. https://docs.rs/rocket/0.4.11/rocket/)
	ex:
	// This will match an HTTP request and utilize the function as its response:
	#[get("/")]
	fn hello() -> &'static str {
		"Welcome to this website!"
	}

