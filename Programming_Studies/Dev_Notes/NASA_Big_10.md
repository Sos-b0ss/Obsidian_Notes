1. Simple Control Flow - don't use goto, setjmp, longjmp, recursion.
2. Limit All Loops - hard limit the number of iterations in all loops.
3. Don't Use the Heap - use only stack memory, don't use malloc or free.
4. Limit Function Size - functions should be no longer than 60 lines.
5. Practice Data Hiding - declare variables in the lowest scope required
6. Check Return Values - explicitly cast all ignored return values to a void type
7. Limit the Preprocessor - limit the use of the C preprocessor to file inclusions and very simple conditional macros, don't use conditional compilation
8. Restrict Pointers Use - pointers should not be able to be dereferenced more than one layer at a time, also don't use function pointers
9. Be Pedantic - compile with all warnings enabled and in pedantic mode, analyze the code with multiple static code analyzers with different rulesets
10. Always, ALWAYS, Unit Test the Code.

These are all very strict and some are way too overkill, but this is a very helpful guideline as to how NASA is able to write such robust and secure code.
