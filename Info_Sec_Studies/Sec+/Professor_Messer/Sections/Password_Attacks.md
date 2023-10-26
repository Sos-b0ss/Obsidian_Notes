Sources:

\
Some applications store passwords "In the clear"
	- No [[Encryption]]. Anyone can read the store passwords.
	- This is rare thankfully, because its incredibly insecure.

Do not store passwords as [[Plaintext]]
	- Anyone with access to the password file or database has every credential.

If your application saves passwords as [[Plaintext]] you really only have the choice to get a better working application.

[[Hashing]] a password

[[Hash]]es represent data as a fixed-length string of text
	- Also known as a [[Message-Digest]] or [[Fingerprint]]
	- Will not have a collision (Different passwords will not have the same [[Hash]])
	- Hashing is one-way so its impossible to recover something from its [[Hash]]
	- Common way to store passwords

example of hash type:
[[SHA-256]]
\
Password files are going to be different on each [[OS]] and it contains all the password hashes for the users on the device.

[Most common passwords wiki](https://en.wikipedia.org/wiki/List_of_the_most_common_passwords)

See. [[Brute_Force]] attack, [[Dictionary_Attack]], [[Rainbow_Tables]], [[Salt]], [[Collection_1]], [[Password_Spraying]]
