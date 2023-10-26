Sources:

\
The [[OSI_Model]] was created to standardize network architecture and encourage vendors to develop network equipment that would avoid proprietary design. It allows any computer system anywhere in the world to communicate with any other, as long as both obey [OSI](https://instrumentationtools.com/7-osi-layers-of-communications/) protocol standards.
\
OSI has codified in the reference model referred to as the: [[OSI-RM]].
\
These are the 7 Layers of the [[OSI_Model]]:
\
![[Pasted image 20220624233612.png]]
\
The services provided by the seven layers of the OSI/RM can be divided into three main regions, as shown below.
\
Network Utilities-layers 7,6, and 5.
\
Host to host transport and internet working – Layers 4, and 3.
\
Sub-network transmission ([[LAN]] and [[WAN]]) – Layers 3,2,1 and Media 0. Layers 3,2,1 and Media 0.
\
Functions of each OSI layer:
\
**[[Application_Layer]]:**
- Layer 7 provides interfaces for applications to access network services such as file sharing, message handling, and data access.
- It also handles error recovery for applications, as desired.
\
**[[Presentation_Layer]]:**
- The presentation layer at level 6, handles data formatting and translation. For outgoing messages, the presentation layer converts data into a format specified by the Application layer, if necessary; for incoming messages, it reverses the conversion if required by the receiving application.
- In short, Layer 6 presents the data in a suitable to the application layer.
- The presentation layer engages protocol conversion, data encryption, decryption, data compression, decompression, data representation incompatibilities between OSI, and graphic commands.
\
**[[Session_Layer]]:**
- Layer 5, the session layer permits two computers to hold ongoing communications-called a session – across a network so applications on either end of the session can swap or exchange data as long as the session lasts.
\
**[[Transport_Layer]]:**
- The transport layer is (Layer 4) manages data transfer from one application to another across a network.
- It breaks long data streams into smaller blocks called “Segments”.
\
**[[Network_Layer]]:**
- The network layer, below the Transport layer, is responsible for routing the packet based on its logical address.
- It moves packets of data from the source to the destination and across the networks if necessary.
\
**[[Data_Link_Layer]]:**
- Layer 2 the data link layer, works with frames and is the mediator between the Network layer and Physical layer.
- It defines how computers access the network medium – also called Media Access Control (MAC), which is why the MAC address is defined at this layer.
\
**[[Physical_Layer]]:**
- The activity of Layer 1 is to convert bits into signals for outgoing messages and signals into bits for incoming messages.
- The type of signal generated depends upon the medium.
- For example, wire media, such as twisted pair cable, use electrical pulses, fiber optic media use pulses of light, and wireless media uses radio waves.
\
**Advantages:**
-   [[OSI_Model]] furnishes the interoperability of diversified communication systems with standard communication and transmission architecture, layers, and protocols.
-   [[OSI_Model]] is an architecture to specify computer network functions in a clear and compatible way.
-   Since protocols are hidden, any protocols can be implemented in this model.
\
**Disadvantages:**
-   It does not define any particular protocol.
-   [[OSI_Model]] is relatively less reliable compared with [[TCP-IP]].

Check out these helpful notes on the OSI model:
![[Screenshot_20230513-125541.png]]