Sources:
https://en.wikipedia.org/wiki/Wi-Fi_deauthentication_attack
https://security.stackexchange.com/questions/20219/preventing-deauthentication-attacks
\
Also known as [[Dissasociation_Attack]]. Its a wifi attack that sends a device that is connected to a wifi [[AP]] a packet that informs it to disconnect from the [[AP]] and when the device tries to automatically connect back to the network generally a [[Rogue_AP]] or [[Evil_Twin]] [[AP]] the bad actor is used to trick the device to connect to it rather than the actual [[AP]] it was connected to prior to the attack.
\
If you are seeing many deauth packets, that is a sign that someone may be trying to attack your wireless network and guess your passphrase. Once the attacker has sent a deauth packet and intercepted the initial handshake, there are tools and online services that automate the task of trying to recover the passphrase, by guessing many possibilities.
