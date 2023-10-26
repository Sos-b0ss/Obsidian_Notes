Rust provides us with a few different ways of creating collections of data of the same type. Two of the most common are the _array_ primitive and the `Vec<T>` type.
\
**Homogenous Collections:**
\
As a general guideline, an array should be used when the collection has a fixed length. When you need a collection that can grow or shrink in size, a Vec should be used.
\
If you are looking to group together data of differing types, consider using a 'tuple', or a 'struct', (See. https://www.codecademy.com/courses/rust-for-programmers/articles/tuples-rust, & https://www.codecademy.com/courses/rust-for-programmers/articles/structs-rust).
\
**Arrays:**
\
Arrays are the most basic homogenous collection in Rust. They have a fixed length, and their data is stored on the stack. This makes arrays very efficient at runtime.
\
An array can be declared with square brackets, [], containing comma separated values.
	ex:

	let integers = [1, 2, 3];

You can initialize the values of an array from an expression rather than manually defining each value. This takes the form of [expression; length] and is useful when creating large arrays.
	ex:

	// This will create an array with 20 chars of value 'e'
	let many_e = ['e'; 20];

	// We can use any expression to populate the default value.
	let initial_value = 'E';
	let more_e = [initial_value.to_ascii_lowercase(); 20];

**Accessing Values:**
\
We can access values of collections using a special syntax referred to as _index expression syntax_. This allows us to directly access a single value or a range of values by index.
\
**Single Values:**
\
We can access a single value of a colection by placing the index of the desired item within square brackets after the collection, 'collection[3]'. It is important to remember that array indexing in Rust, as with most languages, is 0-based.
	ex:

	let array_of_chars = ['a', 'b', 'c'];

	let letter_a = array_of_chars[0]; // 'a'
	let letter_c = array_of_chars[2]; // 'c'

Rather than directly supplying a number, we can utilize any expression which evaluates to the type 'usize'.
	ex:

	fn one() -> usize { 1 }

	let letter_b = array_of_chars[one()]; // 'b'

If we try to access an index that does not exist, our code will not compile.
\
**Ranges:**
\
We can access a range of values from a collection by supplying a beginning and ending index separated by `..` within our index expression.
\
This special syntax is referred to as _rang syntax_. The beginning index is inclusive and the ending index is exclusive.
	ex:

	let words = ["rise", "sun", "ship", "to", "sail"];

	let sunship = &words[1..3]; // ["sun", "ship"]
	println!("{sunship:?}");

If we omit the beginning or ending index, the range will continue until the respective beginning or end.
	ex:

	let head = &words[..2]; // ["rise", "sun"]
	println!("{head:?}");

	let tail = &words[2..]; // ["ship", "to", "sail"]

	let everything = &words[..]; ["rise", "sun", "ship", "to", "sail"];
	println!("{everything:?}");

**Looping/Iteration:**
\
We can operate on the individual values of any collection with 'for' `loops` and `iterators`. (See. https://www.codecademy.com/courses/rust-for-programmers/articles/loops-rust, & https://www.codecademy.com/courses/rust-for-programmers/articles/functional-iteration)
	ex:

	let array_of_chars = ['a', 'b', 'c'];

	// Looping
	for c in array_of_chars {
		println!("{c}");
	}

	// Functional Iteration
	array_of_chars.iter().map(|c| println!("{c}"));

**Vec:**
\
When we need a dynamically sized collection, the std library provides us the `Vec<T>` type. Vec, commonly called a _Vector_, stores its data in the heap, which allows it to grow or shrink in size.
\
There are many 'helpful methods' already available on the Vec type to make development more ergonomic. (See. https://doc.rust-lang.org/std/vec/struct.Vec.html)
\
We can construct Vecs using methods such as new() and from(), but Rust also provides us the `vec![]` macro to allow us to declare a Vec the same way we would an array.
	ex:

	// Initialize a new, empty Vec
	let new_vec: Vec<char> = vec![];

	// Initialize with values
	let vec_of_chars = vec!['a', 'b', 'c'];

	// This is equivalent to the previous example, but utilizing methods
	let mut vec_of_chars = Vec::new();
	vec_of_chars.push('a');
	vec_of_chars.push('b');
	vec_of_chars.push('c');

**Accessing Values:**
\
Like arrays, we can use index expressions to access the values of a Vec. Unlike an array, if we try to access an index that does not exist, our code will successfully compile but will panic at runtime.
\
To avoid this, accessing the values on a Vec is generally accomplished through methods such as 'get()' and 'first()'. These methods return an `Option<T>` which allows us to handle situations where the index does not exist.
	ex:

	let vec_of_chars = vec!['a', 'b', 'c'];

	let a = vec_of_chars.first(); // Some('a')

	// Note that the 'get()' method does not use 0-based indexing
	let c = vec_of_chars.get(2); // Some('c')

	let f = vec_of_chars.get(9); // None

**Other Collections:**
\
The std library has many other collections available such as 'VecDeque', 'BTreeMap', and 'HashMap'. Info about all available collections can be found in Rust's Docs. (See. https://doc.rust-lang.org/std/collections/)
