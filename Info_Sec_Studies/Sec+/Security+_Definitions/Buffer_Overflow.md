Sources:
https://www.geeksforgeeks.org/buffer-overflow-attack-with-example/
https://www.fortinet.com/resources/cyberglossary/buffer-overflow
\
This occurs when Overwriting a [[Buffer]] of memory spills over into other memory areas, this type of action should not ever occur and it could allow an attacker to gain access to something they should not have been able to, or gain escalated privileges.
- This is not a very easy attack to pull off
- Takes time to avoid crashing things
- Takes time to control it and make it do what you want
\
A really useful buffer overflow is repeatable.

| Variable Name | A             |     |     |     |     |     |     |     | B     |    |
| ------------- | ------------- | --- | --- | --- | --- | --- | --- | --- | ---- | --- |
| Value         | [Null String] |     |     |     |     |     |     |     | 1979 |     |
| Hex Value     | 00            | 00  | 00  | 00  | 00  | 00  | 00  | 00  | 00   | 00  |

| Variable Name | A   |     |     |     |     |     |     |     | B    |     |
| ------------- | --- | --- | --- | --- | --- | --- | --- | --- | ---- | --- |
| Value         | 'e' | 'x' | 'c' | 'e' | 's' | 's' | 'i' | 'v' | 25856 |     |
| Hex Value     | 65  | 78  | 63  | 65  | 73  | 73  | 69  | 76  | 65   | 00  |

So This is an example of a buffer overflow occurring, The 'e' that should be at the very end of the word "excessive" was too many characters to fit in the field, therefore it overflowed into variable B's [[Buffer]], and that had changed Variable B's value from 1979 to 25856. This change could very well cause the attacker to either crash the system when ever they want, or access something they should not have been able to.
