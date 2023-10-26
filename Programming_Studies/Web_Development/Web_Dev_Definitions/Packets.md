Sources:

\
In networking, a packet is a small segment of a larger message. Data sent over computer networks, such as the [[Internet]], is divided into packets. These packets are then recombined by the computer or device that receives them.
\
Theoretically, it could be possible to send files and data over the Internet without chopping them down into small [[Packets]] of information. One computer could send data to another computer in the form of a long unbroken line of bits (small units of information, communicated as pulses of electricity that computers can interpret).
\
However, such an approach quickly becomes impractical when more than two computers are involved. While the long line of bits passed over the wires between the two computers, no third computer could use those same wires to send information — it would have to wait its turn.
\
[[Packets]] vs. [[Datagram]]s
\
A [[Datagram]] is a segment of data sent over a packet-switched network. A [[Datagram]] contains enough information to be routed from its source to its destination. By this definition, an [[IP_Packet]] is one example of a [[Datagram]]. Essentially, [[Datagram]] is an alternative term for [[Packets]].
\
**[[IP_Packet]]s:**
\
Packets are sometimes defined by the protocol they are using. A packet with an [[IP_Header]] can be referred to as an [[IP_Packet]]. An [[IP_Header]] contains important information about where a packet is from (its source [[IP_Address]]), where it is going (destination [[IP_Address]]), how large the packet is, and how long network routers should continue to forward the packet before dropping it. It may also indicate whether or not the packet can be fragmented, and include information about reassembling fragmented packets.
\
[[Packet_Headers]]
\
A packet header is a "label" of sorts, which provides information about the packet’s contents, origin, and destination.
\
In practice, packets actually have more than one header, and each header is used by a different part of the networking process. Packet headers are attached by certain types of networking protocols.
\
The packet size of [[IPV6]] is 1280 bytes and the [[IPv4]] packet size is 576 bytes.
