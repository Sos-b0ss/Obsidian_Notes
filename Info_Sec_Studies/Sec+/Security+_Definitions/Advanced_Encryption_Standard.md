Sources:
https://en.wikipedia.org/wiki/Advanced_Encryption_Standard
\
[[AES]] is based on a design principle known as a [substitution–permutation network], and is efficient in both software and hardware. Unlike its predecessor DES, AES does not use a [Feistel network]. AES is a variant of Rijndael, with a fixed [block size] of 128 [bits], and a [key size] of 128, 192, or 256 bits. By contrast, Rijndael _per se_ is specified with block and key sizes that may be any multiple of 32 bits, with a minimum of 128 and a maximum of 256 bits.

The Advanced Encryption Standard ([[AES]]) is defined in each of:
-   FIPS PUB 197: Advanced Encryption Standard ([[AES]])
-   ISO/IEC 18033-3: Block ciphers
\
[[AES]] operates on a 4 × 4 [column-major order] array of bytes, termed the _state_. Most [[AES]] calculations are done in a particular [finite field].

![[Pasted image 20220807174849.png]]
\
Attacks have been published that are computationally faster than a full [brute-force attack], though none as of 2013 are computationally feasible. For AES-128, the key can be recovered with a computational complexity of 2^126.1 using the [biclique attack]. For biclique attacks on AES-192 and AES-256, the computational complexities of 2^189.7 and 2^254.4 respectively apply. [Related-key attacks] can break AES-256 and AES-192 with complexities 2^99.5 and 2^176 in both time and data, respectively.
