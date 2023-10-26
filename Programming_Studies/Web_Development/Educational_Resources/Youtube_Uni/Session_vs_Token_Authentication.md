Source:
https://www.youtube.com/watch?v=UBUNrFtufWo
\
User authentication, there are two main ways to get the job done: sessions and [[Token]]s. The traditional approach on the web is, [[Cookie]]-based, server-side sessions. 
\
The process begins with a user filling out their username and password and then submitting it to a server, which then validates it, creates a session in the database, then responds with a [[Session_ID]]. The [[Session_ID]] will be saved in the browser's cookie jar, which is a place in the browser to save key value pairs that will be sent back to the server on each subsequent request.
\
It can then respond back with content designed for the currently logged in end user. In other words we have a [[Stateful_Session]] between the front-end client and backend server. This approach works great, but there are some drawbacks.
\
It can be vulnerable to an attack known as, [[Cross-Site_Request_Forgery]]. Where the attacker points the user to a site they're logged into to perform actions they didn't intend to do. Like submitting a payment or changing their password. Although the risk is very low especially if you use a modern framework to implement your code, the bigger problem is that you'll need to store the session id in a database or keep it in memory on the server.
\
The fact that most of today's cloud applications are scaled horizontally, this can be a huge bottleneck in production and now that brings us to [[Token-Based_Authentication]], which solves this problem but introduces its own set of challenges.
\
The process begins the same, with the client sending its login details to the server, but instead of storing a session id, it generates a [[JSON_Web_Token]]. The [[JWT]] (pronounced 'JOT') is created with a private key on the server, then it's sent back to the browser, where it's normally kept in local storage.
\
On future requests the [[JWT]] will be added to the [[Authorization_Header]] prefixed by [[Bearer]]. 
ex. "Authorization: Bearer *token*"
\
The server then only needs to validate the signature, there's no need for a database lookup somewhere else in the infrastructure. That's way more efficient when dealing with a distributed system in the cloud.
\
However [[Token]]s can still be hijacked by an attacker and they can also be difficult to invalidate and they can't be used to authenticate a user in the background on the server.
\
## Here's the most important thing to understand:
\
With a **session** the authentication state is handled on the server while **[[Token]]**s are managed on the client.