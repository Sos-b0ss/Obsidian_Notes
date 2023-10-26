Sometimes long chains of 'if else' expressions can get unwieldy and hard to read. When you need to destructure, adding 'if let' expressions into that chain can make it even noisier. This is why Rust provides the 'match' keyword to allow the handling of complex conditional matching in a concise and readable way.

**Match:**
\
A 'match' expression takes a pattern and compares it against any number of provided match arms. You can define match arms with => placed between the matched pattern and its resultant code block.
\
If the body of a 'match' arm is a single statement or expression, you must terminate the block with a `,`.
\
Here is another way of writing an 'if' expression for a boolean value as a 'match':
	ex:

	let there_are_birds = true;

	match there_are_birds {
		true => println!("hooray!"),
		false => {
			println!("don't worry,");
			println!("we can call for them.");
		}
	}
\
**Exhaustiveness:**
\
Match expressions are exhaustive, meaning all possible patterns must be accounted for. You can declare a catch-all arm with the `_` wildcard:
	ex:

	let chosen_number = 3;

	match chosen_number {
		1 => println!("1"),
		2 => printls!("2"),
		3 => printls!("3"),
		_ => printls!("another number"),
	}

Match arms are guaranteed to be processed in order from top to bottom.  After the first successful match is found, its block is returned, and the remaining arms are not checked.
\
**Match Patterns:**

Matches in Rust are really fantastic, thanks to the patterns that can be utilized. All of the following patterns can be used on match arms as well as with 'if' statements.
\
**Or:**
\
You can match multiple values on the same arm with the `|` operator. This is call the 'Or-pattern'.
	ex:

	let plant = "dandelion";

	match plant {
		"dandelion" | "Almond" | "apple" => println!("Rose Family"),
		"tomato" | "pepper" | "potato" => println!("Nightshade Family"),
		_ => println!("not found")
	}

**Ranges:**
\
We can match a range of values with the `..` and `..=` operators to separate our starting and ending index. `..` denotes an exclusive range while `..=` is inclusive:
	ex:

	let chipmunks = 5;

	match chipmunks {
		0 => println!("no chipmunks"),
		1 ..= 20 => println!("some chipmunks"),
		n @ 21 ..= 40 => println!("warning: {n} chipmunks!"),
		_ => println!("too many chipmunks."),
	}

**Binding:**
\
We can bind our matched value to a variable to utilize it in the matched block with the '@' operator:
	ex:

	let chipmunks = 5;

	match chipmunks {
		n @ 0 ..= 40 => println!("warning: {n} chipmunks!"),
		_ => println!("too many chipmunks."),
	}

**Match Guards:**
\
You can even perform additional conditional evaluations on each match arm using an 'if' expression.
	ex:

	let answer = Some("herring");

	match answer {
		Some(x) if x.len() > 7 => {
			println!("incorrect");
			println!("hint: password is less than 7 characters long");
		}
		Some(x) => println!("incorrect"),
		None => {
			println!("");
		}
	}

