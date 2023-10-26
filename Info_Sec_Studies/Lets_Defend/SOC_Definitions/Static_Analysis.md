The information examined during the static analysis is as follows.
\
1.  P.E. (Portable Executable) Headers
2.  Imported DLL's
3.  Exported DLL's
4.  Strings in binary
5.  CPU Instructions
\
It is a fact that mails composed of plain text are boring. For this reason, mail applications provide [[HTML]] support, allowing the creation of mails that can attract more attention of users. Of course, this feature has a disadvantage. Attackers can create e-mails with [[HTML]], hiding [[URL]] addresses that are harmful behind buttons / texts that seem harmless.
\
![[Pasted image 20220710154203.png]]
As seen in the image above, the address that the user sees can be different when the link is clicked (the real address is seen when the link is hovered).
\
(Attackers take a new domain address in most phishing attacks and do a phishing attack within a few days and finish their work. For this reason, if the domain name in the mail is new, it is more likely to be a phishing attack.)
\
It is possible to find out whether the antivirus engines detect the web address as harmful by searching the web addresses in the mail on VirusTotal. If someone else has already analyzed the same address / file in VirusTotal, VirusTotal does not analyze from scratch, it shows you the old analysis result. We can use this feature both as an advantage and a disadvantage.
\
![[Pasted image 20220710154344.png]]
\
If the attacker searches the domain address on VirusTotal without containing harmful content on it, that address will appear harmless on VirusTotal, and if it goes unnoticed, you may be mistaken for this address to be harmless. In the image above, you can see that umuttosun.com address appears harmless, but if you look at the section marked with the red arrow, you will see that this address was searched 9 months ago, and this result is 9 months ago. To have it analyzed again, the button marked with the blue arrow must be pressed.
\
If the page was previously searched on VirusTotal, it may mean that the attacker wanted to see the rate of detection of the site during the preparation phase. If we analyze it again, antivirus engine detects it as phishing, which means that the attacker has a move to trick analysts.
\
Performing static analysis of the files in the mail can enable the learning of the capacity / capabilities of that file. However, since static analysis takes a long time, you can get the information you need more quickly with [[Dynamic_Analysis]].
\
[Cisco Talos Intelligence](https://talosintelligence.com/) has search sections where we can learn reputations of IP addresses. By searching the SMTP address of the mail we detected on Talos, we can see the reputation of the IP address and find out whether it is included in the blacklist. If the SMTP address is in the blacklist, it can be understood that an attack was made on a compromised server.
\
![[Pasted image 20220710161426.png]]
Likewise, the SMTP address can be searched on VirusTotal and [[AbuseIPDB]] to determine if the IP address has previously been involved in malicious activities.
