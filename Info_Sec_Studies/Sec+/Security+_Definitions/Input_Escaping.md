Sources:
http://security.stackexchange.com/questions/32394/ddg#32396
https://learn.microsoft.com/en-us/dotnet/standard/security/security-and-user-input
\
User input is a string. _Escaping_ is done when you want to insert some characters into some [[HTML]] / [[SQL]] / Whatever code which insists on _interpreting_ some characters into special functionalities. For instance, you have a '<' and you want it to be shown back to the user as a '<', but if you brutally paste the string inside the HTML then the Web browser on the client side will look at the '<' and think that it begins some [[HTML]] tag, instead of representing a simple '<'.
\
In general, you want to keep strings as strings, and delegate any encoding or escaping to specialized functions which do that well. For instance, for SQL, you use prepared statements. With HTML from a PHP context, you would use `htmlspecialchars()`.
\
If you are dealing with Web data, consider the various forms of escapes that are permissible, including: Hexadecimal escapes (%nn). Unicode escapes (%nnn). Overlong UTF-8 escapes (%nn%nn). Double escapes (%nn becomes %mmnn, where %mm is the escape for '%'). Be wary of user names that might have more than one canonical format.
