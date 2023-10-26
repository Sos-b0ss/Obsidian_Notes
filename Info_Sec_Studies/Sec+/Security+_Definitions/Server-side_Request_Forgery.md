Sources:
https://portswigger.net/web-security/ssrf
https://www.gcst.ae/server-side-request-forger/
\
A [[SSRF]] is a web security vulnerability that allows an attacker to induce the server-side application to make requests to an unintended location. In a typical [[SSRF]] attack, the attacker might cause the server to make a connection to internal-only services within the organization's infrastructure.
\
**Attacker finds a vulnerable web application:**
- Uses this vulnerability to send specially crafted packets that makes the server preform the request on behalf of the attacker.
- This is always going to be caused by bad programming and insufficient vetting of the code before its sent into production.
- All user input should never be trusted by default
- Servers should always validate their input and the responses
- These are fairly rare, but can be critical vulnerabilities
