Unsolicited message
- Email, forums, etc.
- Spam over instant message ([[SPIM]])

Various content
- commercial advertising
- Non-commercial proselytizing
- Phishing attempts

To prevent spam from taking up resources on your mail server you can implement what's called "tar pitting" to effectively slow down the conversation so that the spammer will just skip over you as a recipient so as to not slow their attack attempt down.
\
You can also implement a spam filter (Email gateway) on either a network level for a mail server or on the application layer itself
- Allowed lists
- [[SMTP]] standards checking
	- blocks anything that doesn't follow [[RFC]] standards
- [[rDNS]] ([[Reverse_DNS]])
	- Block email where the sender's domain doesn't match the [[IP]] address
- Recipient filtering
	- block all email not address to a valid recipient email address
