Sources:
https://www.fortinet.com/resources/cyberglossary/rootkit
\
A common rootkit definition is a type of [[Malware]] program that enables cyber criminals to gain access to and infiltrate data from machines without being detected. It covers software toolboxes designed to infect computers, give the attacker remote control, and remain hidden for a long period of time.
\
Originally a [[Unix]] technique
- The "[[Root]]" in [[rootkit]]

Modifies core system files
- Part of the [[Kernel]]

Can be invisible to the operating system
- Wont see it in Task manager

Example of [[Kernel]] [[Driver]]

Examples of [[Malware]] that started to combine itself with [[Rootkit]]s was with the use of Zeus [[Bots]]/[[Zbot]] [[Malware]]

Now combined the Zeus [[Malware]] with the [[Necurs]] [[Rootkit]]
- [[Necurs]] is a [[Kernel]]-level [[Driver]]

[[Necurs]] makes sure you can't delete [[Zbot]]
- Haha nope, Access denied, no more computer

Trying to stop the windows process?
- Error terminating the [[Process]]: Access denied

New [[UEFI]] "[[Secure_Boot]]" exists to prevent the system from booting from a drive that has had changes made to it therefore avoiding a [[Rootkit]] from being started along with your [[OS]].
