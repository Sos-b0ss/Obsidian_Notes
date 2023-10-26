To help with reading source code in rust, the language likes to seperate constructs by case naming conventions:
\
Like:
\
The 'UpperCamelCase' convention is reserved for types and traits:

	ex.
	struct UnitStruct;

	struct TupleStruct(T); // .. with generic type T

	struct StructName {
		field: NamedTuple,
	}

	enum EnumName {
		VarientName,
	}

	type TypeAlias = u8;

	trait TraitName {}

Items that follow the 'snake_case' convention are reserved for attributes, variables, functions, and macros:


	// Atributes
	#![attribute_name]



	// Variables
	let variable_name = true;



	fn function_name() {
		function_call();
	}



	// Macros
	macro_name!();
	macro_name![];
	macro_name! {};

And then theres the beautiful, 'SCREAMING_SNAKE_CASE', which are resrved for constraints:

	 const EIGHTY_EIGHT: u32 = 80;
