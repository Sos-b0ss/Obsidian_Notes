Readable code is paramount to collaboration and maintainable software. This will introduce the idea that well-named code can sometimes be the best form of documentation.
\
**Type Aliasing:**
\
Being able to define a custom, named type is beneficial in separating out concepts within our code. But sometimes an existing datatype fits our requirements without us needing to define any additional functionality.
\
In these situations, we can provide an alternative name for the type using the 'type' keyword. This is referred to as a _Type Alias_.
	ex:

	// Here we are creating the associated type `Name` which resolves to Rust's `String` type
	type Name = String;

	//This is equivalent to 'Person(String)'
	struct Person(Name);

	fn print_name(person: Person) {
		let name = person.0;
		println!("{}", name);
	}

This does nothing to the original type; aliasing is only a tool to help the programmer better define the codebase.
\
**Import Aliasing:**
\
We can provide alternative names for imports by utilizing the 'as' keyword. This helps to avoid naming conflicts as well as allows us to make our type names concise.
\
Here we will imagine we are using an external crate called 'dataplace' which has an unfortunate internal type named 'String'. Let's redefine some imports to add clarity to our code.
	ex:

	use dataplace::value::String as DbString;
	use std::collections::BTreeMap as Tree;

	fn db_values(values: Vec<(DbString, DbString)>) -> Tree<String, String>
	{
		let mut tree = Tree::new();
		for (k, v) in values {
			tree.insert(k.into(), v.into());
		}
		tree
	}

