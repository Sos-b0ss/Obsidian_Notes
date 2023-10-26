Source:
https://www.w3schools.com/whatis/whatis_http.asp
\
Communication between clients and servers is done by **requests** and **responses**:
\
1.  A client (a browser) sends an [[HTTP_Request]] to the web
2.  A web server receives the request
3.  The server runs an application to process the request
4.  The server returns an [[HTTP_Response]] (output) to the browser
5.  The client (the browser) receives the response
\
A typical [[HTTP]] request / response circle:
\
1.  The browser requests an [[HTML]] page. The server returns an [[HTML]] file.
2.  The browser requests a style sheet. The server returns a [[CSS]] file.
3.  The browser requests an [[JPG]] image. The server returns a [[JPG]] file.
4.  The browser requests [[JavaScript]] code. The server returns a [[JS]] file
5.  The browser requests data. The server returns data (in [[XML]] or [[JSON]]).
\
All browsers have a built-in **XMLHttpRequest Object ([[XHR]])**.
\
[[XHR]] is a JavaScript object that is used to transfer data between a web browser and a web server.
\
[[XHR]] is often used to request and receive data for the purpose of modifying a web page.
\
Despite the XML and Http in the name, XHR is used with other protocols than [[HTTP]], and the data can be of many different types like [[HTML]], [[CSS]], [[XML]], [[JSON]], and plain text.
\
The [[XHR]] Object is a **Web Developers Dream**, because you can:
\
-   Update a web page without reloading the page
-   Request data from a server - after the page has loaded
-   Receive data from a server - after the page has loaded
-   Send data to a server - in the background
\
The [[XHR_Object]] is the underlying concept of [**AJAX**](https://www.w3schools.com/whatis/whatis_ajax.asp) and [[JSON]].
