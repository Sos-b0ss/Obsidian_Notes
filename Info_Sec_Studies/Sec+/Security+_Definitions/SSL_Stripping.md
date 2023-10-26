Sources:
https://comodosslstore.com/blog/what-is-ssl-stripping-beginners-guide-to-ssl-strip-attacks.html
https://cybersophia.net/articles/what-is/what-is-ssl-stripping-attack-and-how-to-avoid-it/
\
Also known as [[HTTP]] downgrade, it combines an on-path attack with a downgrade attack:
- Fairly difficult to implement, but big returns for the attacker
- Attacker had to sit in the middle of the conversation so they may either be using a [[Proxy_Server]], [[ARP]] [[Spoofing]], or a rogue wifi hotspot ([[Rogue_AP]]), etc.
- Must modify data between the victim and the web server
\
SSL Stripping is an attack used to circumvent the security provided by [[HTTPS]] connections between the users and the [[HTTPS]] enabled websites. This attack is also known as [[SSL]] Downgrade Attack, since it downgrades secure [[HTTPS]] connections to [[HTTP]] and exposes the traffic exchanged in [[Plaintext]] (unencrypted) to eavesdroppers.
