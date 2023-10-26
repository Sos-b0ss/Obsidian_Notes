Sources:
https://www.cyber-recon.com/glossary/driver-manipulation/
https://www.youtube.com/watch?v=0EI0Rs1QAes
\
Cyber-Recon Device drivers allow an operating system ([[OS]])such as [[Windows]] to talk to hardware devices such as printers. Sophisticated attackers may dive deep into the device drivers and manipulate them so that they undermine security on your computer.
\
Traditional [[Antivirus]] is very good at identifying known attacks
- Checks the signature
- Block everything that matches
\
There's still ways [[Bad_Actor]]s find to infect, hide, and maintain persistence. It's a constant battle against [[Zero-Day]] attacks, new attack types and strategies, [[Nation_State]]s etc.
\
Often times [[Malware]] likes to attack your device by either infecting or impersonating your device [[Driver]]s.
- [[Driver]]s are very powerful because they are essentially a conduit between your hardware and your [[OS]]
\
[[Shimming]] is something that is commonly used on windows called the [[Windows_Compatibility_Mode]].
\
This allows for:
- Backwards compatibility with previous [[Windows]] Versions
- Application Compatibility [[Shim]] [[Cache]]
\
Shims like this are able to be abused by Malware authors. They found out that they can write their own Shims to get around security like [[UAC]].
\
This exact vulnerability was discovered in January 2015
\
Another way that attackers found out how to get around Anti-Virus from catching the [[Malware]] is by using what's called [[Refactoring]] also known as writing [[Metamorphic_Malware]] by having random code strings added on or loops added onto the code so as to make it a different program and be undetectable by anti-malware software.

---

[[Driver_Manipulation]] can occur when [[OS]]s have a need to operate with an older [[Driver]] in order to maintain compatibility. Windows 10, for example, needed to have compatibility with windows 8 drivers. In some cases, the code needs to be "[[Shim]]med," wherein calls to the older [[Driver]] are intercepted and set to [[Shim]] code that bridges the gap between the environments.
\
Reference:
CompTIA Security+ Certification Study Guide, Fourth Edition. Pg 624.
Mike Meyers' CompTIA Security+ Certification Guide, Third Edition. Pg 276-277.
