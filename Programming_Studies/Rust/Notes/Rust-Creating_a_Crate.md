Keep in mind the only 3 programs you need to start programming in rust is:
	- rustc [The rust compiler]
	- rustup [Used to manage the version of rust]
	- cargo [This is the main tool used during development]
\
With cargo, a project is called a 'packages, and packages can consist of multiple crates.
\
To start off a new program you can either choose to create a .rs file named whatever you want your program to be named, and then you want to 
start it with a function like this hello world example:
\
	ex.
fn main(){
	println!("Hello World");
}
\
Notice that you use 'println' similarly to in python, and you want to make certain that after each command in the function you have a semicolon at the end, similarly to in js. Then wrap the function in curly braces and then just run in the terminal:
	rustc foobar.rs
(Where foobar is the name of your program you chose to make)
\
Alternatively to start writing your own crate you can also just use the command:
	cargo new foobar
In the terminal and it will create a folder named "foobar" with the following as the directory structure:
	- src/
		- main.rs
	- cargo.toml
\
All the rust source code will be kept in the src directory. The Cargo.toml serves as the configuration file for the crate.
\
If youre wanting to create a library instead of an executable you can use the '--lib' flag like:
	cargo new --lib foobar
\
This will create a lib.rs in our src/ directory instaed of a main.rs file.
	-src/
		-lib.rs
	cargo.toml
\
When creating a binary crate like this, Cargo will provide you with the following code in the 'main.rs' file:
	fn main(){
		println!("Hello World!");
	}
\
This is because all binary programs require a 'main()' function which serves as the entry point for the program. If you run the program with 'cargo run foobar' then the terminal will print out: "Hello World!"
\
Library Crates have no point of entry, but it is important to remember that we will need to manually export items we want users of the library to be able to access.
