Sources:
https://www.geeksforgeeks.org/replay-attack/
https://www.techopedia.com/definition/21695/replay-attack
\
Useful information is sent over the network and a crafty hacker will take advantage of this.
\
This could be anything from [[Login_Credentials]] to [[Session_ID]]'s
\
This attack can be done physically from an actual [[Network_Tap]] installed on the line that allows the attacker to redirect the flow of data back to their workstation. They could also use a logical way of attacking such as [[ARP_Poisoning]], or they could just flat out use [[Malware]] installed on the victim's computer.
\
The gathered information may help the attacker replay the data to appear as someone else. The freighting part of this [[Attack_Vector]] is that the attacker does not even have to be on the network at the time of the attack to gain the benefit from it also known as an [[On-Path_Attack]]. They can just process the replay at a later date so long as they gained the right data to replay.
\
This is a very common way to wage a "[[Pass_The_Hash]]" attack.
\
A way to prevent this type of attack from working is if the developers make the application on each of the devices communicate on the network using [[SSL]] or [[TLS]] encryption or salt the [[Hash]] so it can only be used once. So that way it doesn't matter what hash the attacker manages to intercept, it will be encrypted and they will be unable to send the proper passphrase to decrypt the [[Hash]] and gain access.
\
This is a reason that we should always make sure the cookies within the browser is secure, because if an attacker gains access to your cookies on the network they may have access to your [[Session_ID]]s and they could gain access to your previous login sessions and preform what's known as a [[Side-jacking]] attack or [[Session_Hijacking]].
\
Common ways attackers are able to gain access to this information in the first place is by using tools like:
- [[Wireshark]]
- [[Kismet]]

To scope out the network for certain traffic attackers will commonly use tools like:
- [[Tamper]]
- [[Firesheep]]
- [[Scapy]]

to utilize [[Header_Manipulation]] and discover if the server has an [[XSS]] vulnerability and if it does then they could just have the server send all the login [[Session_ID]]s sent to them directly rather then them needing to intercept the actual users attempting to log-in.
