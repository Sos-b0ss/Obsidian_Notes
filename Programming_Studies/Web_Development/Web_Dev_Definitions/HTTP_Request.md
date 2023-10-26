Source:
https://www.tutorialspoint.com/http/http_requests.htm
\
This can occur within a [[Browser]], or a client software designed to access information from webpages.
\
An [[HTTP]] [[Client]] sends an [[HTTP_Request]] to a server in the form of a request message which includes following format:
\
-   A [[Request-line]]
-   Zero or more header (General|Request|Entity) fields followed by [[CRLF]]
-   An empty line (i.e., a line with nothing preceding the [[CRLF]])
    indicating the end of the header fields
-   Optionally a message-body
\
The [[Request-line]] begins with a [[Method_Token]], followed by the [[Request-URI]] and the protocol version, and ending with [[CRLF]]. The [[Element]]s are separated by space [[SP_Character]]s.
\
[[Request-line]] = [[Method_Token]] [[SP_Character]] [[Request-URI]] [[SP_Character]] [[HTTP]]-Version [[CRLF]]
