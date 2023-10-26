Sources:
https://en.wikipedia.org/wiki/Cross-site_request_forgery
https://portswigger.net/web-security/csrf
\
Cross-site request forgery, also known as one-click attack or [[Session_Riding]] and abbreviated as [[CSRF]] or [[XSRF]], is a type of malicious exploit of a website where unauthorized commands are submitted from a user that the web application trusts.
\
This type of attack occurs by abusing the trust a website has for:
- Your [[Browser]]
- [[HTTP_Request]]s are made without your consent or your knowledge
- [[HTTP_Request]]s and [[HTTP_Post]]s made to look like you had preformed them

It is a request that is sent by your computer essentially committing forgery of your login credentials.
\
Ways developers can prevent this from happening is by using anti-forgery techniques, or by using cryptographic [[Token]]s that only the real user would have access to.
\
Example of this would be:
- A [[Hyperlink]] sent in an email that sends the victim to a specific page of their banking website that is still recognizing that they were logged in to send their bank account money.
