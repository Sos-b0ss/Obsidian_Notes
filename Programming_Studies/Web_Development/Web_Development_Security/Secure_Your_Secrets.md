If you dont rewrite your githistory then secrets like your passwords used will still be in there for anyone to go back and find.
\
Secrets can be anything like an [[API_Key]], might be a client secret, or credentials for authentication.
\
Number 1 rule with secrets is DONT check them into source control, you can use tools like [[Gitguardian]] and this will actually notify you if you happen to check in any secrets into the source control. [[netlify]] and [[AWS]] actually happen to do this by default.
Apply this EVEN in a private repo!
\
A lot of this concern can be avoided if you just be sure to use environment variables and if you are sure to encrypt your secrets, use tools like: [[HashiCorp_Vault]] which has Spring support and there is also [[Azure_Key_Vault]], which is similar to Amazon's key management service.
\
Check here for more details:
https://developer.okta.com/blog/2020/05/04/spring-vault
\
