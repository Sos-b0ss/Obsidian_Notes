[[TCP]] (transmission Control Protocol)
\
If ever asked to draw out the [[TCP]] steps, draw out
a 3 way handshake:
\
If this handshake ever has an error it will terminate and restart
\
-->
syn
<--
syn/ack
-->
ack w/ data
\
[[TCP]] is needed because it is connection oriented and makes sure that every byte is sent in order and will resend if anything has an error.
It does this with a [[3-way handshake]]. It also needs to do a [[termination]] ([[4 way handshake]]) to actually send the data properly.
\
-->
[[FIN]]
<--
[[ACK]]
<--
[[FIN]]
-->
[[ACK]]
\
This is all the basics for [[TCP]].
\
downsides of [[TCP]]
\
[[TCP_Re-transmission]] (when the server re-sends [[Packets]] because the [[Client]] does not acknowledge receipt) verifying this transmission can be slow.
to avoid this slower response time you can use [[UDP]] (User Datagram Protocol) and it will only send and respond instead.
\
-->
Request
<--
Response
\
It doesn't actually need to check if the packets arrive, if the packets don't arrive it doesn't stop or retry it just keeps sending packets.
\
When trying to flood a network or [[IP]] you can look at [[UDP_Flooders]]. Just make sure not to flood with too many or else it will also boot yourself off the network.
