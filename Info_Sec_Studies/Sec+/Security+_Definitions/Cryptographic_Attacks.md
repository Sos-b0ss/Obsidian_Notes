Sources:
https://www.packetlabs.net/posts/cryptography-attacks/
https://www.valencynetworks.com/blogs/cyber-attacks-explained-cryptographic-attacks/
https://threat.media/definition/what-is-a-cryptographic-attack/
\
A cryptographic attack is a method used by hackers to target cryptographic solutions like ciphertext, encryption keys, etc. These attacks aim to retrieve the [[Plaintext]] from the [[Cypher]]text or decode the encrypted data.
\
How do you know that your data is secure that you're sending to another person by email?
\
When the bad guy doesn't have the key, they just break the safe to get what's inside.
\
The problem is hardly ever the cryptography, its often the way that its applied.
\
[[Birthday_Attack]]:
\
Say in a group of 23 students, the chance of two students sharing a birthday is about 50%, so for a class of 30 students, the chance is about 70%.
\
One example of a hash collision happened with an [[MD5]] hash, and because the hash was not secure enough, in 2008 Researchers created a [[CA]] certificate that appeared to be legit and issued by [[RapidSSL]]
\
[[Downgrade_Attack]]:
\
In 2014 some researchers discovered the TLS vulnerability [[POODLE]] by sitting in the middle of a conversation between two devices, also known as an [[On-Path_Attack]] and they had forced the clients to fallback to [[SSL_3.0]]. The reason they did this was because SSL 3.0 has significant cryptographic vulnerabilities. Because of [[POODLE]], modern web-browsers wont ever fall back to [[SSL_3.0]]
