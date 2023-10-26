Sources:
https://en.wikipedia.org/wiki/Ticket_Granting_Ticket
https://doubleoctopus.com/security-wiki/authentication/ticket-granting-tickets/
\
In some computer security systems, a [[Ticket_Granting_Ticket]] or Ticket to Get Tickets is a small, encrypted identification file with a limited validity period. After [[Authentication]], this file is granted to a user for data traffic protection by the [[Key_Distribution_Center]] subsystem of authentication services such as [[Kerberos]]. The [[TGT]] file contains the session key, its expiration date, and the user's [[IP]] address, which protects the user from man-in-the-middle ([[MITM]]) attacks.
\
In [[Kerberos]] authentication, a [[TGT]] is a user authentication token issued by the [[Key_Distribution_Center]] ([[KDC]]) that is used to request access tokens from the [[Ticket_Granting_Service]] ([[TGS]]) for specific resources/systems joined to the domain.
