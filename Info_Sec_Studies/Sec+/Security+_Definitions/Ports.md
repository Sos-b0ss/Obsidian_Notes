Sources:
https://www.geeksforgeeks.org/50-common-ports-you-should-know/
\
Port numbers in computer networking represent communication endpoints. Ports are unsigned 16-bit integers (0-65535) that identify a specific process, or network service. [[IANA]] is responsible for internet protocol resources, including the registration of commonly used port numbers for well-known internet services. 
\
[[Well_Known_Ports]]: 0 through 1023.  
[[Registered_Ports]]: 1024 through 49151.  
[[Dynamic_Private_Ports]]: 49152 through 65535.  
\
[[TCP]] ports use the Transmission Control Protocol, the most commonly used protocol on the Internet and any [[TCP]]/[[IP]] network. [[TCP]] enables two hosts to establish a connection and exchange streams of data. [[TCP]] guarantees delivery of data and that [[Packets]] will be delivered in the same order in which they were sent. Guaranteed communication/delivery is the key difference between [[TCP]] and [[UDP]].  
\
[[UDP]] ports use the Datagram Protocol. Like [[TCP]], [[UDP]] is used in combination with IP (the Internet Protocol) and facilitates the transmission of datagrams from one computer to applications on another computer, but unlike [[TCP]], [[UDP]] is connectionless and does not guarantee reliable communication; it's up to the application that received the message to process any errors and verify correct delivery. [[UDP]] is often used with time-sensitive applications, such as audio/video streaming and Realtime gaming, where dropping some packets is preferable to waiting for delayed data.
\
You can check for open port on a network by sending a [[SYN]]/[[ACK]] request to every port on the network, and if you get a response the port is open. 
\
This process is called a [[SYN_Scan]]
\
[[Nessus]]/[[Nmap]] will automate the port scanning process.
\
there are 3 states of [[Ports]]:
- Opened (allowing packets to come and go)
- Closed (not allowing any communication)
- [[Filtered]] (possible [[Firewall]])
\
[[Wireshark]] can also be used to display requests to show if a port is opened or closed.
