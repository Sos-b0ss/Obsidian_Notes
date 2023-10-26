Sources:
https://owasp.org/www-community/Improper_Error_Handling
https://www.techopedia.com/definition/16626/error-handling
\
Error handling refers to the response and recovery procedures from error conditions present in a software application. In other words, it is the process comprised of anticipation, detection and resolution of application errors, programming errors or communication errors. Error handling helps in maintaining the normal flow of program execution.
\
Improper handling of errors can introduce a variety of security problems for a web site. The most common problem is when detailed internal error messages such as [[Stack_Traces]], [[Database_Dump]]s, and [[Error_Code]]s are displayed to the user (hacker). These messages reveal implementation details that should never be revealed.
