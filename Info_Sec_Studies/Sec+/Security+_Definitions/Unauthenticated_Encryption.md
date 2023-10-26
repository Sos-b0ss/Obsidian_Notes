Sources:
https://cookmyproject.com/blog/unauthenticated-encryption/
\
[[Encryption]] should always be authenticated. There are two common solutions to this: Add a [[Message_Authentication_Code]] ([[MAC]]). This is a keyed cryptographic [[Checksum]] that provides authenticity and integrity. Use an authenticated mode of operation such as [[GCM]]. Even with this advice, there are many pitfalls.
