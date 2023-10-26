Sources:
https://www.geeksforgeeks.org/challenge-handshake-authentication-protocol-chap/
\
In computing, the Challenge-Handshake Authentication Protocol is an authentication protocol originally used by Point to Point Protocol to validate users. [[CHAP]] is also carried in other [[Authentication]] protocols such as [[RADIUS]] and [[Diameter]]. Almost all network operating systems support [[PPP]] with [[CHAP]], as do most network access servers.
\
Its used at the initial startup of the link, but also does periodic checkups to make sure the router is still talking to the same host. It uses a 3-way handshake (not like [[TCP]]). It uses [[MD5]], and offers more security than [[PAP]]. Requires you knowing the plaintext of the secret sent over the network. There are 4 types of [[CHAP]] packets.

- [[Challenge_Packet]]
- [[Response_Packet]]
- [[Success_Packet]]
- [[Failure_Packet]]
