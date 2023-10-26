When working with 'References', we sometimes must be explicit in how long a particular reference lives before it is dropped from memory. Rust introduced the concept of _Lifetimes_ to be able to handle these situations. (See. https://www.codecademy.com/courses/rust-for-programmers/articles/references-rust)
\
**The Borrow Checker:**
\
The 'rustc' compiler has a built-in system that looks at the scopes of references and checks to make sure that no references are dropped before we try to use them.
\
Here is the most rudimentary example of what is being scrutinized by the borrow checker.
	ex:

	First we declare an empty variable
	let a;
	{
		let b = true; // Then we create the variable 'b' with the value 'true'
		a = &b; // Here we are assigning our 'a' value to be a reference to 'b'.
	} // At this point, the value of 'b' is dropped because it is now out-of-scope.

	// We can no longer access 'a' because the value it's referencing no longer exists.
	//println!("{}", a)

Many times lifetimes an be determined by the compiler, so we do not always have to declare them explicitly. There are certain rules that are used to make this determination. These are referred to as _lifetime elision rules_.
\
**Annotating Lifetimes:**
\
We can annotate a lifetime on a reference by appending the `&` with a `'label`. Lifetimes are generic in nature and are usually denoted with simple names such as `'a` and `'b`
	ex:

	let live: &'a str = "This will live for the life of `'a`";

When we create a data structure with lifetimes, we must annotate the lifetime on the field as well as on our new type directly. Lifetime annotations for custom types occur between `<>` placed after the name of our data structure.
	ex:

	struct Outfielder<'a> {
		name: &'a str,
	}

	// We can declare multiple lifetimes by separating them with commas.
	struct Batter<'a, 'b> {
		name: &'a str,
		stance: &'b str,
	}

We must also annotate functions in the same manner.
	ex:

	fn pass_to<'a>(name: &'a str) -> String {
		format!("Passing the ball to {name}")
	}

When we are declaring an 'impl' block for a type that utilized lifetimes, we must also annotate it directly. Lifetimes are inherently passed to all contained methods, so we do not require explicit annotations on methods.
	ex:

	impl<'a> Outfielder<'a> {
		fn pass_to(name: &'a str) -> String {
			format!("Passing the ball to {name}")
		}
	}

**The 'static Lifetime:**
\
There is a special lifetime annotation of `'static` which defines a lifetime as being capable of living for the duration of our program. This is commonly encountered when declaring &str constants.
	ex:

	cont LONG_LIVED: &'static str = "Life is beautiful";

Sometimes we can quickly resolve lifetime issues by declaring them as `'static`, but we should consider whether we really need the lifetime to live that long.
\
**Generics and Lifetimes:**
\
Generic and lifetime annotations are located in the same place. When we have both generics and lifetime annotations for the same item, we always declare lifetimes first.
	ex:

	use std::fmt::Disply;

	// Lifetimes and generic annotations are separated by commas.
	pub fn pass_to<'a, T: Display>(name: &'a T) {
	println!("Passing the ball to {name}")
	}
