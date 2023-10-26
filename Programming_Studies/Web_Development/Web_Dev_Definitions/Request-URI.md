Sources:
https://www.tutorialspoint.com/http/http_requests.htm
\
The Request-[[URI]] is a Uniform Resource Identifier and identifies the resource upon which to apply the request. Following are the most commonly used forms to specify an [[URI]]:
\
Request-URI = "*" | absoluteURI | abs_path | authority


| S.N. | Method and Description                                                                                                                                                                                                                                                                      |
| ---- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | The asterisk is used when an [[HTTP_Request]] does not apply to a particular resource, but to the server itself, and is only allowed when the method used does not necessarily apply to a resource.                                                                                          |
| 2    | The **absoluteURI** is used when an [[HTTP_Request]] is being made to a proxy. The proxy is requested to forward the request or service from a valid cache, and return the response. For example: **GET http://www.w3.org/pub/WWW/TheProject.html HTTP/1.1**                                 |
| 3    | The most common form of Request-URI is that used to identify a resource on an origin server or gateway. For example, a client wishing to retrieve a resource directly from the origin server would create a TCP connection to port 80 of the host "www.w3.org" and send the following lines: |
| -    | **GET /pub/WWW/TheProject.html HTTP/1.1**                                                                                                                                                                                                                                                    |
| -    | **Host: www.w3.org**                                                                                                                                                                                                                                                                         |
| -    | Note that the absolute path cannot be empty; if none is present in the original [[URI]], it MUST be given as "/" (the server root).                                                                                                                                                              |
