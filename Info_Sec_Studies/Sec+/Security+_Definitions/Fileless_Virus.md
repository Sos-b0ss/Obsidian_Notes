Sources:
https://www.fortinet.com/resources/cyberglossary/fileless-malware
\
Fileless [[Malware]] is malicious code that works directly within a computer's memory instead of the hard drive. It uses legitimate, otherwise benevolent programs to compromise your computer instead of malicious files. It is fileless" in that when your machine gets infected, no files are downloaded to your hard drive.
\
A steal attack
- Does a good job of avoiding [[Antivirus]] detection

Operates in memory
- but never installed in a file or application

Ex. :
User clicks on malicious website link > Website exploits a [[Flash]]/[[Java]]/[[Windows]] vulnerability > Launches [[PowerShell]] and downloads payload in [[RAM]] > Runs [[PowerShell]] scripts and [[Executable]]s in memory, ex-filtrates data, damages files > Adds an auto-start to [[Registry]]
