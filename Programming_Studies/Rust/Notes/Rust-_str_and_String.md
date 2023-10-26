Managing strings of characters such as "this short sentence." is a common task handled by most languages. Rust gives us flexibility for the best performance possible by providing us with two different string types: &str and String.
\
The important difference between these types is that &str is an immutable reference to data in memory, while a String is a collection that allows composition and mutation.
\
**&str:**
\
A &str is an immutable 'slice' of bytes of a fixed size, and is often referred to as a "string slice". (See. https://www.codecademy.com/courses/rust-for-programmers/articles/references-rust) Since a &str is only a reference to data, our type declarations will always have the preceding '&'.
\
The data of a &str is stored on the stack, which makes them computationally efficient.
	ex:

	let immutable = "I am a location in memory";

	// A type annotated str.
	let value: &str = ", and cannot be mutated.";

	let baked: &'static str = "I am baked into the binary!";

	println!("{immutable} {value}");
	println!("{baked}");

Since a '&str' is immutable, we cannot do much with them other than validate them and access their data. Whenever we do not know the size of our string or plan on manipulating the value, we should utilize the 'string' type.
\
**String:**
\
A 'String' is stored on the heap, which allows us to mutate the value at will. While heap memory is never as fast as the stack, the heap allows Rust to automatically resize the allocated memory when needed during runtime.
	ex:

	let empty_string = String::new();
	let value_stromg = String::from("Cyan");

	let mut mutable_string = String::from("Indigo");
	mutable_string.push_str(" and Maroon.");

	println!("{mutable_string}");

If we lok at the source code for the std library, we can see that a String is actually a `Vec<u8`. This allows us to utilize 'iterators' and other methods accessible on `Vec<T>`. (See. https://www.codecademy.com/courses/rust-for-programmers/articles/functional-iteration)
\
Strings are very ergonomic in terms of how we can compose them. Concatenation can be accomplished in all the following ways.
	ex:

	let a = "Welcome";
	let b = " to";
	let c = " the";
	let d = " show!";

	let welcome1 = format!("{a}{b}{c}{d}");
	let welcome2 = [a,b,c,d,"!"].concat();
	let welcome3 = a.to_string() + b + c + d + "!";

	// We can even append to a mutable String with the '+=' operator.
	let mut welcome4 = welcome3;
	welcome4 += " Lets have some fun!";

Dynamically sized data types such as String do not implement the Copy trait because its data is stored on the heap. This means we cannot derive Copy on structs that have Strings as fields.
\
In these circumstances, we should utilize 'Clone' to duplicate our data when needed. (See. https://doc.rust-lang.org/std/clone/trait.Clone.html)
\
## Conversions:
\
**&str to String:**
\
We can turn a '&str' into a String using the 'String::from()' or "to_string()" method. Both are commonly utilized in Rust, and using one over the other is a matter of personal preference.
	ex:

	let pinapple = "pineapple";

	let new_string = String::from(pineapple);
	let new_string = pineapple.to_string();

**String to &str:** To utilize a String as a '&str', we only have to reference the value.
	ex:

	fn say_fruit(name: &str) {
		println!("{name}")
	}

	let papaya = String::from("Papaya");

	say_fruit(&papaya);

**UTF-8:**
\
Rust's strings utilize 'UTF-8' encoding. This is a global standard that allows representations of most all written languages and many symbols, including emojis.
	ex:

	let latin = "corderoy";
	let greek = "τίποτα χώρο";
	let maths = "ℇ ℎ ⋉ ⊻ ⊽ ∞ ⋊";
	let suits = "♠ ♥ ♦ ♣":
	let emojis = "😑😑😀";

UTF-8 is a dynamically sized encoding scheme. This means that some single-width characters are actually multiple bytes combined to form a single symbol.
	ex:

	// These take up the same amount of memory.
	let wow1 = "wow";
	let wow2 = "☽";

	println!("{} == {}", wow1.len(), wow2.len());

**Other Strings:**
\
Most current operating systems do not encode strings in UTF-8 and instead utilize their own standards of encoding. Rust provides as the 'OsStr' and 'OsString' types to safely interact with these systems. (See. https://doc.rust-lang.org/std/ffi/struct.OsStr.html, & https://doc.rust-lang.org/std/ffi/struct.OsString.html) types to safely interact with these systems.
\
For interacting with "null-terminating" strings or the C programming language, Rust provides us the 'CStr' and 'CString' types. If you're not familiar with C, try the 'Learn C' course at Codecademy: https://www.codecademy.com/learn/learn-c. (See. https://doc.rust-lang.org/std/ffi/struct.CStr.html, & https://doc.rust-lang.org/std/ffi/struct.CString.html)
\
These types are designed so that there is little to no performance penalty when converting between them and their respective &str and String types.
