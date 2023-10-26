The most straightforward way of creating our own macros is with 'macro_rules!'. 'Macros' made with this special macro are known as 'Declarative Macros' and they are a quick way for us to start manipulating our source code. (See. https://www.codecademy.com/courses/rust-for-programmers/articles/macros-rust)

The downside to using declarative macros is that they can be hard to debug. Even though the Rust compiler is very sophisticated, we sometimes end up with erroneous errors caused by a small type in a macro body.
\
**Macro_rules!:**
\
Declarative macros allow us to take syntactic fragments of the Rust language as input and then return raw source code. A big bonus of declarative macros is that they allow arbitrary repetition of code.
\
A 'macro_rules!' declaration takes the following form:
	ex:

	macro_rules! make_it {
		() => {
			// Everything placed here will be generated in source code when the macro is called.
		}
	}

Here we have begun making a macro with the name "make_it!". We will handle all our input within `()` and all our output within `{}`.
\
Let's begin by making our macro print a character to stdout.
	ex:

	macro_rules! make_it {
		() => {
			print!('r')
		}
	}

A macro that takes no input is still very useful for importing large amount of code, but macros are much more powerful when we have input, so let's add some.
\
**Input:**
\
When working with macros, parameters are referred to as _Metavariables_, and their respective types are called _fragment-specifiers_.
\
We can declare our metavariables in a similar manner as function parameters. However, metavariables must start with '$', and there can be no spaces between the metavariables, its fragment-specifier, and the separating `:`.
	ex:

	macro_rules! make_it {
		($happen:expr) => {
			println!("{}", $happen)
		}
	}

	make_it!("we did it!");
	make_it!(usize::MAX);

Here we have let our macro accept any expression which we can represent with the metavariable '$happen' and passing it to 'println!(())'.
\
Some commonly used fragment-specifiers other than 'expr' include 'ident' for identifiers, 'stmt' for statements, 'ty' for types, and 'literal' for literals. A complete list of fragment-specifiers can be found in 'The Rust Reference'. (See. https://doc.rust-lang.org/reference/macros-by-example.html)
\
**Repetition:**
\
The best part about macros is how easy it is to repeat fragments of code. We can repeat code by enclosing it within `$()` followed by either a `*`, `+`, or `?`.
- `*` will accept any number of repetitions, including none.
- `+` with accept any number of repetitions, but requires at least one.
- `?` will accept one or no repetitions.

Lets spice up our 'make_it!' macro with some repetition.
	ex:

	macro_rules! make_it {
		( $var:ident => $($count:expr),+) => {
			$($var.push($count);)+
		}
	}

	let mut count = vec![];

	make_it![count => u8::MIN, 1, 2];

	println!("{count:?}");

Now we can 'push()' a comma separated list of expressions into an existing variable.
\
By adding the `,` to create `$(),+` in our input, we are stating that the repeated items are delimited by `,`. We can use any single token as a delimiter that is valid in the context of nearby metavariables.
\
**Exporting:**
\
Macros can be exported and used anywhere in our crate with the `#[macro_export]` attribute. This also makes the macro visible to other crates when importing our crate as a dependency.
	ex:

	#[macro_export]
	macro_rules! make_it {
		( $var:ident => $($count:expr),+) => {
			$($var.push($count);)+
		}
	}

Alternatively, we can also export all macros contained within a module with the `#[macro_use]` attribute.
	ex:

	#[macro_use]
	mod macros;

Macros from external crates can be imported like any other item, but we can also utilize `#[macro_use]` to do so.
\
The examples of declarative macros we have used in this article are basic, but the concepts are far-reaching and can accomplish powerful things.
