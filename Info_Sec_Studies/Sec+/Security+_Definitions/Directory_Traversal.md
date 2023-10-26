Sources:
https://portswigger.net/web-security/file-path-traversal
https://www.acunetix.com/websitesecurity/directory-traversal/
\
Directory traversal (also known as file path traversal) is a web security vulnerability that allows an attacker to read arbitrary files on the server that is running an application. This might include application code and data, credentials for back-end systems, and sensitive operating system files.
\
Directory traversal or Path Traversal is an [[HTTP]] attack that allows attackers to access restricted directories and execute commands outside of the web [[server]]'s root directory. Web [[Server]]s provide two main levels of security mechanisms 
- Access Control Lists ([[ACL]]s)
- Root directory 

An Access Control List is used in the authorization process. It is a list which the web server’s administrator uses to indicate which users or groups are able to access, modify or execute particular files on the server, as well as other access rights.
