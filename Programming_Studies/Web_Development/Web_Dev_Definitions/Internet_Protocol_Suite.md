Sources:
https://www.elprocus.com/internet-protocol-suite-and-its-architecture/
\
Originally [[TCP]] was divided into two protocols those are:
\
- [[TCP]] (Transmission Control Protocol)
- [[IP]] (Internet Protocol).
\
\
It is one type of protocol and network model used on the internet. It consists of four layers: [[Application_Layer]], [[Transport_Layer]], [[Internet_Layer]], and the [[Link_Layer]]. 
\
In this networking, the [[TCP]] and the [[IP]] layers are the most widely used protocols, so that this model named as [[TCP-IP_Model]] or [[Internet_Protocol_Suite]] model.
\
Let us take two hosts one is a client and another is a server. For example, the client has opened a webpage that is having some services and in the next step, the client wants to upload records or data or files. Whenever the client wants to upload or update the record that the request goes to the server. 
\
Suppose the client or user wants to change the settings of an email, then the settings will reach to the server. This can be done using the [[TCP-IP_Model]] and this process goes to the [[Transport_Layer]] and reaches the network. The [[Transport_Layer]] act as a host of the system and the process reaches to the network with the help of cables. The internet protocol suite architecture is shown in the below figure.
\
![[Pasted image 20220624213516.png]]
\
**Internet Protocol Suite Layers**
\
The [[TCP]]/[[IP]] model classified into two types they are four-layer [[TCP]]/[[IP]] model and five [[TCP]]/[[IP]] models. The layer numbers start from the bottom and go up. The classification of the [[TCP]]/[[IP]] model shown in the below figure:
\
![[Pasted image 20220624213612.png]]
\
**1. Four Layer [[TCP-IP_Model]]:** The four-layer [[TCP-IP_Model]] consists of four layers are [[Application_Layer]], [[Transport_Layer]], [[Internet_Layer]], and [[Link_Layer]]. The layer number, layer name, and protocol name are shown in the below table.
\
| **Layer Number** | **Layer Name**    | **Protocol Name**                |
| ---------------- | ----------------- | -------------------------------- |
| 4.               | Application Layer | [[HTTP]], [[Telnet]], [[DNS]], [[SNMP]], [[DHCP]]    |
| 3.               | Transport Layer   | [[TCP]], [[UDP]]                         |
| 2.               | [[Internet]] Layer    | [[IP]], [[ICMP]], [[IGMP]]                   |
| 1.               | Link Layer        | Ethernet, Wireless LAN, [[PPP]], [[ARP]] |
\
**2) Five Layer TCP/IP model:** The solution of this link layer is to divide the link layer into two different layers. The [[Datalink_Layer]] and the [[Physical_Layer]] are two layers and this is how the five-layer [[TCP-IP_Model]] is made. Now a day’s in the industry level all the people are using the five-layer [[TCP-IP_Model]].
\
| **Layer Number** | **Layer Name**    | **Protocol Name**                                 |
| ---------------- | ----------------- | ------------------------------------------------- |
| 5.               | [[Application_Layer]] | [[HTTP]], [[Telnet]], [[DNS]], [[SNMP]], [[DHCP]] | 
| 4.               | [[Transport_Layer]]   | [[TCP]], [[UDP]]                                  |
| 3.               | [[Network_Layer]]     | [[IP]], [[ICMP]], [[IGMP]]                        |
| 2.               | [[Datalink_Layer]]    | [[LAN]], [[PPP]], [[ARP]]                             |
| 1.               | [[Physical_Layer]]    | Ethernet, Wireless                                |
\
The five-layer [[TCP]]/[[IP]] protocol has five layers they are [[Application_Layer]], [[Transport_Layer]], [[Network_Layer]], [[Datalink_Layer]], and [[Physical_Layer]]. The [[Physical_Layer]] is the first layer which is mainly focused on hardware like Ethernet and wireless [[LAN]], the second layer is [[Datalink_Layer]], which is mainly focused on the software portion like [[PPP]] and [[ARP]], the third layer is [[Network_Layer]], the fourth layer is [[Transport_Layer]], and the fifth layer is [[Application_Layer]]. In the four-layer [[TCP-IP_Model]], we have an [[Internet layer]] and in the five-layer [[TCP-IP_Model]] we have a [[Network_Layer]], both layers have the same sort of functionality.
