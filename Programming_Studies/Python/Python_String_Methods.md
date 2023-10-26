"Hello World".capitalize() --> Hello world
"Hello World".casefold() --> Hello world
"Hello World".count("o") --> 2
"Hello World".find("World") --> 6
"Hello World".index("Hello") --> 0
"Hello World".isalnum() --> False
"Hello World".isalpha() --> False
"Hello World".isascii() --> True
"Hello World".isdecimal() --> False
"Hello World".isdigit() --> False
"Hello World".isidentifier() --> False
"Hello World".islower() --> True
"Hello World".isnumaric() --> False
"Hello World".isprintable() --> True

1. upper() and lower(): Need to convert your string to uppercase or lowercase? These methods have got your back! upper() converts all characters in a string to uppercase, while lower() does the opposite by converting them to lowercase. They're perfect for normalizing user input or manipulating text effortlessly.
2. capitalize(): Want to capitalize the first character of a string? This method does precisely that! It converts the first character to uppercase and keeps the rest as lowercase. It's ideal for transforming names or titles into a consistent format.
3. strip(), lstrip(), rstrip(): These methods are real lifesavers when it comes to handling whitespace in strings. Strip() removes leading and trailing whitespace, while lstrip() and rstrip() specifically remove whitespace from the left or right side of the string, respectively. They're essential for cleaning up user inputs or processing text files with ease.
4. split() and join(): Splitting and joining strings are common operations in text processing. split() breaks a string into a list of substrings based on a delimiter, which is useful when you want to extract individual words or tokens. On the other hand, join() concatenates a list of strings into a single string using a specified separator.
5. replace(): Need to replace specific substrings with a string? This method is your go-to solution! Simply provide the substring to be replaced and the replacement string. It's invaluable for text manipulation tasks, like finding and replacing particular words or characters.

