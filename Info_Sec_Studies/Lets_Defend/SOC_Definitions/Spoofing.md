Sources:

\
Attackers can send emails on behalf of someone else, as the emails do not necessarily have an authentication mechanism. Attackers can send mail on behalf of someone else using the technique called spoofing to make the user believe that the incoming email is reliable. Several protocols have been created to prevent the Email [[Spoofing]] technique. With the help of [[SPF]], [[DKIM]] and [[DMARC]] protocols, it can be understood whether the sender's address is fake or real. Some mail applications do these checks automatically. However, the use of these protocols is not mandatory and in some cases can cause problems.
\
To find out manually whether the mail is spoof or not, [[SMTP]] address of the mail should be learned first. [[SPF]], [[DKIM]], [[DMARC]] and [[MX_Record]]s of the domain can be learned using tools such as [Mxtoolbox](https://mxtoolbox.com/). By comparing the information here, it can be learned whether the mail is spoof or not.
\
Since the [[IP_Address]]es of the big institutions using their own mail servers will belong to them, it can be examined whether the [[SMTP]] address belongs to that institution by looking at the [[Whois]] records of the [[SMTP]] [[IP_Address]].
\
An important point here is that if the sender address is not spoofed, we cannot say the mail is safe. Harmful mails can be sent on behalf of trusted persons by hacking corporate / personal email addresses. This type of cyber attacks has already happened, so this possibility should always be considered.
