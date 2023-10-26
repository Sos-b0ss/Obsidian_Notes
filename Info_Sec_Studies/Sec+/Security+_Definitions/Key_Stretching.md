Sources:
https://en.wikipedia.org/wiki/Key_stretching
https://www.massgymnastics.org/stretching/which-algorithm-can-be-used-for-key-stretching-solution-found.html
https://cryptobook.nakov.com/mac-and-key-derivation/hmac-and-key-derivation
\
In cryptography, key stretching techniques are used to make a possibly weak key, typically a password or passphrase, more secure against a brute-force attack by increasing the resources it takes to test each possible key. Passwords or passphrases created by humans are often short or predictable enough to allow password cracking, and key stretching is intended to make such attacks more difficult by complicating a basic step of trying a single password candidate. Key stretching also improves security in some real-world applications where the key length has been constrained, by mimicking a longer key length from the perspective of a brute-force attacker. There are several ways to perform key stretching. One way is to apply a cryptographic hash function or a [[Block_Cypher]] repeatedly in a loop. For example, in applications where the key is used for a cipher, the key schedule in the cipher may be modified so that it takes a specific length of time to perform.
\
Key Stretching Purpose Key stretching techniques use salts. Two common key stretching techniques are [[Bcrypt]] and Password-Based Key Derivation Function 2 ([[PBKDF2]]): [[Bcrypt]]. Based on the [[Blowfish]] [[Block_Cipher]], [[Bcrypt]] is used on many [[Unix]] and [[Linux]] distributions to protect the passwords stored in the shadow password file ([[Shadow_File]]).
\
Simply calculating hash_func(key + msg) to obtain a [[MAC]] (message authentication code) is considered insecure (see the details). It is recommended to use the [[HMAC]] algorithm instead, e.g. [[HMAC]]-[[SHA-256]] or [[HMAC]]-SHA3-512 or other secure [[MAC]] algorithm.
\
Salting a password is a technique used in key stretching to make the password more secure against cracking attempts. There are various techniques to stretch a key; some are more common but each is different.
[[PBKDF2]] is a salting technique that incorporates a pseudo-random function to protect passwords of at least 64 bits. [[PBKDF2]] is in many applications, such as [[Wi-Fi]] Protected Access II ([[WPA2]]), Apple's [[iOS]] mobile operating system, and Cisco operating systems.
\
Reference:
Mike Meyers' CompTIA Security+ Certification Guide, Third Edition. Pg 146.
