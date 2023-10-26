See. [[Subnet]]
\
Definition of [[CIDR]] = Classless Inter-Domain Routing whenever you see a / after an IP address it is using [[CIDR_Notation]]
\
192.168.8.0/25 (the 25 is borrowing 1 bit from 
255.255.255.0 	this [[Subnet]] mask because its 1+24 and 24 is the normal [[CIDR_Notation]] for 1 network)
->[128] 64 32 16 8 4 2 1 (by borrowing 1 bit that means that its going to be using the 128 at the beginning of this [[Binary]] set)
make sure to always sum each bit that gets borrowed so if the CIDR was 26 then it would be borrowing 2 bits (24+2) and then the subnet mask for each of the networks created would be using (128+64) at the end of the mask
\
255.255.255.128
\
Network Equation:
2(n) = Networks
ex. [2^(1) = 2 networks]
\
Host Equation:
2(n)-2 = Host
ex. [2^(7)-2 = 126]
\
The reason the 7 is in there is because of the fact that in this situation if the original IP was 192.168.8.0/25 because its borrowing a bit to split up the two networks and the reason the second network ip is going to start with the 255 is because the second
\
To specify a range of IPs on a networks using an IP understand that the 
\
0 1-126 127
\
"192.168.8.1-126"
\
128 129-254 255
\
"192.168.8.129-254"
\
If there is ever not a 0 at the end of subnet mask the network is using [[Subnet_Mask]]ing. 

________________________________________________________________________________________

ex.
\
Computer A
192.168.8.25
255.255.255.128
\
Computer B
192.168.8.130
255.255.255.128
\
Both of these IPs are on different networks and are using [[Subnet_Mask]]ing because of the [128] that follows the [[Subnet_Mask]]
\
This means that both of these devices will not be able to ping and receive a response. Even if both of these computers are hard connected they would not speak to each-other because they both think they are on completely different networks.
\
The only way to remedy this would be to connect both devices to a router because routers are specifically used to connect two networks that are dissimilar to each-other.
\
This is useful for splitting up entire networks between departments like if computer A was marketing and Computer B was HR department that would prevent any possibility of both the devices sharing data with each-other.

________________________________________________________________________________________
ex.
\
192.168.8.0/27
\
Original Class: 
	Class C [255.255.255.0]
New Class: 
	Class C [255.255.255.244]
How many networks: 
	8 networks [2^(3)-2]
How many hosts: 
	30 hosts [2^(5)-2]
\
Range for each network:
________________________________________________________________________________________

256 - 224 = 32
0 	1-30 31 	[Network ID: 0   | Broadcast ID:  31] ex. 192.168.8.0/31
32 	33-62 63 	[Network ID: 32  | Broadcast ID:  63] ex. 192.168.8.32/63
64 	65-94 96 	[Network ID: 64  | Broadcast ID:  96] ex. 192.168.8.64/96
96 	97-126 127 	[Network ID: 96  | Broadcast ID: 127] ex. 192.168.8.96/96
128 	129-158 159 	[Network ID: 128 | Broadcast ID: 159] ex. 192.168.8.128/159
160 	161-190 191 	[Network ID: 160 | Broadcast ID: 191] ex. 192.168.8.160/191
192 	193-222 223	[Network ID: 192 | Broadcast ID: 223] ex. 192.168.8.192/223
224 	225-286 287	[Network ID: 224 | Broadcast ID: 287] ex. 192.168.8.224/287
