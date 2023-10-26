Sources:
https://www.ibm.com/docs/en/zos/2.4.0?topic=operation-cipher-feedback-cfb-mode
\
The [[CFB]] mode uses an initial chaining vector ([[ICV]]) in its processing. [[CFB]] mode performs [[Cypher]] feedback [[Encryption]]. [[CFB]] mode operates on segments instead of blocks. The segment length (called s ) is between one bit and the block size (called b) for the underlying algorithm ([[DES]] or [[AES]]), inclusive.
