Sources:
https://www.geeksforgeeks.org/what-is-bridge-protocol-data-unit-bpdu-frame/
\
Bridge Protocol Data Unit is fundamentally a tree traversed convention which portrays each message of the organization with the various sorts of characteristics on the organization like the [[MAC]] address or the [[IP]] address utilizing distinctive switch ports present on the organization.  
\
The [Spanning Tree Protocol](https://www.geeksforgeeks.org/types-of-spanning-tree-protocol-stp/) ([[STP]]) can empower and impair every one of the switches in a specific region network like [[LAN]] (neighborhood) or [[PAN]] (individual) region network so the course of trade of data stays flawless and the crossing tree calculation might turn out appropriately for the system’s administration. 

### Types of BPDU
\
There are basically two types of [[BPDU]]s:

-   **Configuration BPDUs:** Configuration [[BPDU]]s are mainly used in the presence of the network root bridge where they are responsible for controlling and authenticating the outward flow of data and act as a [[Firewall]] of protection from outside.
     
-   **Topology Change Notification ([[TCN]]) BPDUs:** [[Topology_Change_Notification]] ([[TCN]]) [[BPDU]]s maintain upward data streaming where it continuously regulates which network topologies are being used currently and it notifies with a reminder when the topology changes.
