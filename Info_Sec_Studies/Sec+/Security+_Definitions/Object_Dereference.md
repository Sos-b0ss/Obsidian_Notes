Sources:
https://owasp.org/www-community/vulnerabilities/Null_Dereference
https://stackoverflow.com/questions/64050115/what-exactly-does-mean-the-term-dereferencing-an-object
https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/pointer-related-operators
\
"Dereferencing an object" means "obtain the variable pointed by a pointer".
\
Dereferencing means following the reference to access the actual underlying object. If the reference is `null`, this causes a big problem.
