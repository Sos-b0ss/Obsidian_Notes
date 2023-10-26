Sources:
https://www.cloudflare.com/learning/security/threats/cross-site-scripting/
https://www.fortinet.com/resources/cyberglossary/cross-site-scripting
https://owasp.org/www-community/attacks/xss/
https://www.geeksforgeeks.org/what-is-cross-site-scripting-xss/
\
[[Cross_Site_Scripting]] is often abbreviated to [[XSS]]. Rather than the commonly used [[CSS]] which is associated with web development languages like [[HTML]] and [[JavaScript]]. A vulnerability that allows data from one site to be shared with another site.
- The name was derived from a browser security flaw that allowed information from one site to be shared to another one.
- One of the most common web application development errors 
- Takes advantage of a user's trust for the site
- Complex and Varied

There are Malware that uses Cross-site scripting attacks

[[Non-persistent_(reflected)_XSS_Attack]]:
- Web site allows scripts to run in user input
- Search boxes are a very common source
- The attacker emails a very specific type of link that takes advantage of this vulnerability
- Runs a script the sends credentials/[[Session_ID]]s/[[Cookie]]s to the attacker
\
You can try this by using the testing tool [[Web_Goat]]

[[Persistent_XSS]]:

- Attacker posts a message to a social network that includes a malicious payload.
- Everyone that reads that malicious post or image, they get infected by the [[Script]].

ex.
On June 2017 Aaron Guzman a Security Researcher had noticed that while authenticating with Subaru.com they had received a login token that never expired.
- This allowed the user to enter the token at a later date and the website thinks that it is actually them accessing the site as if they had logged in.
- This token even allowed any service request even changing the email address on file linked to your account.

This is the reason why you never want to click an unknown link that is sent to you via email.
\
Another option is to allow you to disable [[JavaScript]] on your browser, however this is a highly unpractical solution given most of the [[Internet]] uses [[JavaScript]].
