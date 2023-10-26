Rust, like most programming languages, allows us to control the flow of code execution by repeating a block of code. This repeating behavior can be endless or bounded by conditional evaluation.
\
**Loop:**
\
We can repeat a block of code endlessly with the 'loop' statement:
	ex:

	println!("This is the program that never ends...");

	loop {
		print!(" yes, it goes on and on, my friend,")
	}
\
**Break and continue:**
\
Code execution within a loop can be diverted at any point with the 'break' and 'continue' keywords.
\
'break' will stop code execution and exit the loop:

	loop {
		println!("I will be printed once");
		break;
		println!("I will not be printed");
	}

'continue' will stop code execution and restart at the beginning of the loop:
	ex:

	loop {
		print!(".");
		continue;
		println!("I wil not be printed");
	}

	println!("I will also never print");

**Loop Labels:**
\
When we have multiple nested loops, we may want to 'break' out of a parent loop directly rather than the one we are currently in. Rust allows us to take our loops with labels utilizing the syntax 'label: loop {}'.
\
We can then denote which loop we want to break out of by its label.
	ex:

	'first: loop {
		println!("entering 'first'");

		'second: loop {
			println!("entering 'second");
			break 'first;
		}
		println!("I will never print")
	}

**While:**

We can repeat code based on a conditional evaluation with the 'while' statement. Once the provided condition is satisfied, the loop will break.
\
This is an implementation of the previous example using a 'while' statement:
	ex:

	let mut number = 0;

	while number <= 11 {
		println!("{number}");
		number += 2;
	}

Note that we can still use 'break' and 'continue' within 'while' statements to control its looping behavior.
\
**While let:**
\
We can destructure with a 'while' statement using the 'while let' pattern. This pattern operates much the same way an 'if let' pattern does.
\
This is particularly useful when utilizing mutable monadic types:
	ex:

	let mut timer = Some(10);

	while let Some(seconds_left) = timer {
		if seconds_left == 0 {
			println!("done!");
			timer = None;
		} else {
			println!("{seconds_left}");
			std::thread::sleep_ms(1000);
			timer = Some(seconds_left - 1);
		}
	}

**For/in:**
\
It is possible to iterate over the items of a collection utilizing the 'for' and 'in' keywords. Any collection which implements the 'std::iter::Iterator' trait can utilize this pattern.
	ex:

	let numbers = vec![10, 9, 8, 7, 6, 5, 4, 3, 2, 1,];

	println!("the numbers are ");

	// Here 'n' is a newly created variable for each item of our collection.
	for n in numbers {
		println!("{n} ");
	}

Another way to approach looping over collections is through functional iteration. (See. https://www.codecademy.com/courses/rust-for-programmers/articles/functional-iteration)
