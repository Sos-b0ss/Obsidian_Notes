r.Crow666A reference is a way of pointing to a particular piece of data within memory. By referencing existing data, we can re-use that data without needing to allocate additional memory.
\
Since memory is managed manually in rust, references are found everywhere and can help make it very performant.
\
**&**
Every time a value is declared with let, data is created thats stored in memory. A reference to that data can then be created by prefixing the expression with the & prefix.
\
In this example, 'funny_number' is a reference to 'pi':

	let pi = 3.14159265359;
	let funny_number = &pi;

	println!("{funny_number}");

References can also be created pointing to other references:
	ex.

	let lightspeed = 299792458;

	let fast = &lightspeed;
	let still_fast = &&lightspeed;

	let speed_of_light = &still_fast; // This is equivalent to &&&lightspeed

**Dereference:**
When you need to access the underlying data a reference points to directly, you can 'dereference' with the '*' prefix:
	ex.

	let mut year = 3020;
	let y = &mut year;

	*y +10;

	println!("The year is {year}.");

**Automatic Dereferencing:**
\
The Rust compiler will automatically dereference whenever possible, specifically when the '.' operator is used. Here theres no worry about manually dereferencing 'earth' because the call to 'to_uppercase()' will accomplish this already:

	let planet = "Earth";
	let earth = &&&&planet;

	assert_eq!("EARTH", earth.to_uppercase());

**ref:**
Sometimes a reference to the inner values of a complex data structure is needed.
\
When accessing an inner value by reference, you might need to utilize the 'ref' keyword which permits this functionality:

	let starship: Option<String> = Some("Omaha".to_string());

	match starship {
		Some(ref name) => println!("{}", name),
		None => {}
	}

	\\ Without the use of the 'ref' keyword above, this next line would not compile:
	println!("{:?}", starship);

You can also use 'ref' with mutable data with 'ref mut':
	ex.

	let mut planet: Option<String> = Some("Waleco 8".to_string());

	match planet {
		Some(ref mut name) => {
			name.push('8');
		}
		None => {}
	}

ref technically accomplishes the same thing as '&' but is placed on the other side of the assignment. In this way, they can be thought of as reciprocals of each other.
	ex.

	let val = "reciprocal";

	let ref r1 = val;
	let r2 = &val;

	assert_eq!(r1, r2);

**Slices:**
\
A reference to a range of elements from a collection is called a 'slice'. To take a slice you would use index expressions on a referenced collection:
	ex.

	let s = String::from("hello world");

	let hello = &s[0..5];
	let world = &s[6..11];
	println!("{hello}{world}");

For more info on slices, check out the "Accessing Ranges" section of the "Array" and "Vec" article:
https://www.codecademy.com/courses/rust-for-programmers/articles/arrays-and-vec
