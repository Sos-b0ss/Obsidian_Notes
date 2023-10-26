Sources:
https://resources.infosecinstitute.com/certification/the-security-cbk-domains-information-and-updates/
\
25% of the CompTIA SEC+ exam exam:
\
This domain covers the implementation of secure protocols, host or application security solutions, wireless security settings and secure solutions for mobile devices and the cloud, given real-world scenarios. This also includes [[Identity_Control]], [[Authentication]], [[Authorization]], [[PKI]] and account management in general.
\
Other required concepts include the practical use of tunneling/[[VPN]]/[[PPP]] (e.g., for site-to-site connections or providing users with [[Remote_Access]]), correctly placing security devices such as [[Firewall]]s, Sensors([[Card_Sensors]], [[Temperature_Sensors]], [[Moisture_Detection]]), collectors and protecting [[SDN]] (software-defined networking) in an enterprise environment. Another important task is implementing secure systems design to safeguard aspects related to Hardware([[HSM]])/[[Firmware]] security, operating systems ([[OS]]s) and [[Peripheral]]s.
\
This is also the domain that covers questions on endpoint security [[ETDR]] (latest [[Antivirus]]/[[AV]], [[Anti-malware]] and intrusion prevention systems [[IPS]]) as well as how to harden the entire company [[IT]] structure, how to secure applications and work with security protocols.
# 3.0 Implementation

---

## 3.1 Given a scenario, implement secure protocols.
- [ ] • Protocols
	-Domain Name System Security Extensions ([[DNSSEC]])
	-[[SSH]]
	-Secure/Multipurpose Internet Mail Extensions ([[SMIME]])
	-Secure Real-time Transport Protocol ([[SRTP]])
	-Lightweight Directory Access Protocol Over SSL ([[LDAPS]])
	-File Transfer Protocol, Secure ([[FTPS]])
	-SSH File Transfer Protocol ([[SFTP]])
	-Simple Network Management Protocol, version 3 ([[SNMPv3]])
	-Hypertext transfer protocol over [[SSL]]/[[TLS]] ([[HTTPS]])
	-[[IPSec]]
	-Authentication header ([[AH]])/ Encapsulating Security Payloads ([[ESP]])
	-Tunnel/transport
	-Post Office Protocol ([[POP]])/ Internet Message Access Protocol ([[IMAP]])
- [ ] • Use cases
	-Voice and video
	-Time synchronization
	-Email and web
	-File transfer
	-Directory services
	-Remote access
	-Domain name resolution
	-Routing and switching
	-Network address allocation
	-Subscription services

## 3.2 Given a scenario, implement host or application security solutions.
- [ ] • Endpoint protection
	-Antivirus
	-Anti-malware
	-Endpoint detection and response ([[EDR]])
	-[[DLP]]
	-Next-generation firewall ([[NGFW]])
	-Host-based intrusion prevention system ([[HIPS]])
	-Host-based intrusion detection system ([[HIDS]])
	-Host-based firewall
- [ ] • Boot integrity
	-Boot security/Unified Extensible Firmware Interface ([[UEFI]])
	-[[Measured_Boot]]
	-[[Boot_Attestation]]
- [ ] • Database
	-[[Tokenization]]
	-[[Salt]]ing
	-[[Hashing]]
- [ ] • Application security
	-[[Input_Validation]]s
	-Secure [[cookie]]s
	-Hypertext Transfer Protocol ([[HTTP]]) headers
	-Code signing
	-Allow list
	-Block list/deny list
	-Secure coding practices
	-Static code analysis
	-Manual code review
	-Dynamic code analysis
	-[[Fuzzing]]
- [ ] • Hardening
	-Open [[ports]] and [[services]]
	-[[Registry]]
	-Disk encryption
	-[[OS]]
	-Patch management
	-Third-party updates
	-Auto-update
- [ ] • Self-encrypting drive ([[SED]])/ full-disk encryption ([[FDE]])
	-Opal
- [ ] • Hardware root of trust
- [ ] • Trusted Platform Module ([[TPM]])
- [ ] • Sandboxing

## 3.3 Given a scenario, implement secure network designs.

---
- [ ] • Load balancing
	-Active/active
	-Active/passive
	-Scheduling
	-Virtual IP
	-Persistence
- [ ] • Network segmentation
	-Virtual local area network ([[VLAN]])
	-[[Screened_Subnet]] (previously known as demilitarized zone [[DMZ]])
	-East-west traffic
	-[[Extranet]]
	-[[Intranet]]
	-[[Zero_Trust]]
- [ ] • Virtual private network ([[VPN]])
	-Always-on
	-Split tunnel vs. full tunnel
	-[[Remote_Access]] vs. site-to-site
	-[[IPSec]]
	-[[SSL]]/[[TLS]]
	-[[HTML5]]
	-Layer 2 tunneling protocol ([[L2TP]])
- [ ] • [[DNS]]
- [ ] • Network access control ([[NAC]])
	-Agent and agentless
- [ ] • Out-of-band management
- [ ] • Port security
	-Broadcast storm prevention
	-Bridge Protocol Data Unit (BPDU) guard
	-Loop prevention
	-Dynamic Host Configuration Protocol (DHCP) snooping
	-Media access control (MAC) filtering
- [ ] • Network appliances
	-Jump servers
	-Proxy servers
	-Forward
	-Reverse
	-Network-based intrusion detection system ([[NIDS]])/network-based intrusion prevention system ([[NIPS]])
	-Signature-based
	-Heuristic/behavior
	-Anomaly
	-Inline vs. passive
	-[[HSM]]
	-Sensors
	-Collectors
	-Aggregators
	-Firewalls
	-Web application firewall ([[WAF]])
	-[[NGFW]]
	-[[Stateful]]
	-[[Stateless]]
	-Unified threat management ([[UTM]])
	-Network address translation ([[NAT]]) gateway
	-Content/[[URL]] filter
	-Open-source vs. proprietary
	-Hardware vs. software
	-Appliance vs. host-based vs. virtual
- [ ] • Access control list ([[ACL]])
- [ ] • Route security
- [ ] • Quality of service ([[QoS]])
- [ ] • Implications of [[IPv6]]
- [ ] • Port spanning/port mirroring
	-[[Port_Tap]]s
- [ ] • Monitoring services
- [ ] • File integrity monitors

## 3.4 Given a scenario, install and configure wireless security settings.

---
- [ ] • Cryptographic protocols
	-WiFi Protected Access 2 ([[WPA2]])
	-WiFi Protected Access 3 ([[WPA3]])
	-[[Counter_Mode_CBC-MAC_Protocol]] Protocol ([[CCMP]])
	-Simultaneous Authentication of Equals ([[SAE]])
- [ ] • Authentication protocols
	-Extensible Authentication Protocol ([[EAP]])
	-Protected Extensible Authentication Protocol ([[PEAP]])
	-[[EAP-FAST]]
	-[[EAP-TLS]]
	-[[EAP-TTLS]]
	-[[IEEE]] 802.1X
	-Remote Authentication Dial-in User Service ([[RADIUS]]) Federation
- [ ] • Methods
	-Pre-shared key (PSK) vs. Enterprise vs. Open
	-WiFi Protected Setup (WPS)
	-Captive portals
- [ ] • Installation considerations
	-Site surveys - Heat maps
	-WiFi analyzers
	-Channel overlaps
	-Wireless access point (WAP) placement
	-Controller and access point security

## 3.5 Given a scenario, implement secure mobile solutions

---
- [ ] • Connection methods and receivers
	-Cellular
	-[[Wi-Fi]]
	-[[Bluetooth]] [[BT]]
	-[[NFC]]
	-Infrared [[IR]]
	-[[USB]]
	-Point-to-point [[P2P]]
	-Point-to-multipoint
	-Global Positioning System ([[GPS]])
	-[[RFID]]
- [ ] • Mobile device management ([[MDM]])
	-Application management
	-Content management
	-Remote wipe
	-Geofencing
	-Geolocation
	-Screen locks
	-Push notifications
	-Passwords and [[PIN]]s
	-[[Biometrics]]
	-Context-aware authentication
	-Containerization
	-Storage segmentation
	-Full device encryption ([[FDE]])
- [ ] • Mobile devices
	-MicroSD hardware security module (HSM)
	-MDM/Unified Endpoint Management (UEM)
	-Mobile application management (MAM)
	-SEAndroid
- [ ] • Enforcement and monitoring of:
	-Third-party application stores
	-[[Rooting]]/jailbreaking
	-Sideloading
	-Custom [[firmware]]
	-Carrier unlocking
	-Firmware over-the-air ([[OTA]]) updates
	-Camera use
	-[[SMS]]/Multimedia Messaging Service ([[MMS]])/Rich Communication Services ([[RCS]])
	-External media
	-[[USB]] On-The-Go ([[USB_OTG]])
	-Recording microphone
	-[[GPS]] tagging
	-[[Wi-Fi]] direct/[[Ad_hoc]]
	-[[Tethering]]
	-[[Hotspot]]
	-Payment methods
- [ ] • Deployment models
	-Bring your own device ([[BYOD]])
	-Corporate-owned personally enabled ([[COPE]])
	-Choose your own device ([[CYOD]])
	-Corporate-owned
	-Virtual desktop infrastructure ([[VDI]])

## 3.6 Given a scenario, apply cybersecurity solutions to the cloud.

---
- [ ] • Cloud security controls
	-High availability across zones
	-Resource policies
	-Secrets management
	-Integration and auditing
	-Storage
	-Permissions
	-Encryption
	-Replication
	-High availability
	-Network
	-Virtual networks
	-Public and private subnets
	-Segmentation
	-[[API]] inspection and integration
	-Compute
	-Security groups
	-Dynamic resource allocation
	-Instance awareness
	-Virtual private cloud ([[VPC]]) endpoint
	-[[Container]] security
- [ ] • Solutions
	-[[CASB]]
	-Application security
	-Next-generation secure web gateway ([[SWG]])
	-Firewall considerations in a cloud environment
	-Cost
	-Need for segmentation
	-Open Systems Interconnection ([[OSI]]) layers
- [ ] • Cloud native controls vs. third-party solutions

## 3.7 Given a scenario, implement identity and account management controls.

---
- [ ] • Identity
	-Identity provider ([[IdP]])
	-Attributes
	-Certificates
	-Tokens
	-[[SSH]] keys
	-Smart cards
- [ ] • Account types
	-User account
	-Shared and generic accounts/credentials
	-Guest accounts
	-Service accounts
- [ ] • Account policies
	-Password complexity
	-Password history
	-Password reuse
	-Network location
	-Geofencing
	-Geotagging
	-Geolocation
	-Time-based logins
	-Access policies
	-Account permissions
	-Account audits
	-Impossible travel time/risky login
	-Lockout
	-Disablement

## 3.8 Given a scenario, implement authentication and authorization solutions.

---
- [ ] • Authentication management
	-Password keys
	-Password vaults
	-[[TPM]]
	-[[HSM]]
	-Knowledge-based authentication
- [ ] • Authentication/authorization
	-[[EAP]]
	-Challenge-Handshake Authentication Protocol ([[CHAP]])
	-Password Authentication Protocol ([[PAP]])
	-802.1X
	-[[RADIUS]]
	-Single sign-on ([[SSO]])
	-Security Assertion Markup Language ([[SAML]])
	-Terminal Access Controller Access Control System Plus ([[TACACS+]])
	-[[OAuth]]
	-[[OpenID]]
	-[[Kerberos]]
- [ ] • Access control schemes
	-Attribute-based access control ([[ABAC]])
	-Role-based access control
	-Rule-based access control
	-[[MAC]]
	-Discretionary access control ([[DAC]])
	-Conditional access
	-Privileged access management
	-Filesystem permissions

## 3.9 Given a scenario, implement public key infrastructure.

---
- [ ] • Public key infrastructure ([[PKI]])
	-Key management
	-Certificate authority ([[CA]]) 
	-Intermediate [[CA]]
	-Registration authority ([[RA]]) 
	-Certificate revocation list ([[CRL]])
	-Certificate attributes
	-Online Certificate Status Protocol ([[OCSP]])
	-Certificate signing request ([[CSR]])
	-[[CN]]
	-Subject alternative name
	-Expiration
- [ ] • Types of certificates
	-Wildcard
	-Subject alternative name
	-Code signing
	-Self-signed
	-Machine/computer
	-Email
	-User
	-[[Root]]
	-Domain validation
	-Extended validation
- [ ] • Certificate formats
	-Distinguished encoding rules ([[DER]])
	-Privacy enhanced mail ([[PEM]])
	-Personal information exchange ([[PFX]])
	-[[.cer]]
	-[[P12]]
	-[[P7B]]
- [ ] • Concepts
	-Online vs. offline [[CA]]
	-[[Stapling]]
	-[[Pinning]]
	-[[Trust_Model]]
	-[[Key_scrow]]
	-[[Certificate_Chaining]]

# Acronyms used in this domain of the exam:

---

[[ABAC]]
[[ACL]]
[[AH]]
[[AV]]

[[BYOD]]

[[CA]]
[[CASB]]
[[CCMP]]
[[CHAP]]
[[CN]]
[[COPE]]
[[CRL]]
[[CSR]]
[[CYOD]]

[[DAC]]
[[DER]]
[[DNSSEC]]

[[EAP]]
[[ESP]]
[[ETDR]]

[[FDE]]
[[FTPS]]

[[GPS]]

[[HSM]]
[[HTML5]]
[[HTTPS]]
[[HTTP]]

[[IdP]]
[[IEEE]]
[[IMAP]]
[[IPv6]]
[[IPS]]
[[IR]]
[[IT]]

[[L2TP]]
[[LDAPS]]

[[MAC]]
[[MDM]]
[[MMS]]

[[NAC]]
[[NAT]]
[[NFC]]
[[NGFW]]
[[NIPS]]
[[NIDS]]

[[OCSP]]
[[OSI]]
[[OTA]]

[[PAP]]
[[PEAP]]
[[PEM]]
[[PFX]]
[[PIN]]
[[PKI]]
[[POP]]
[[PPP]]
[[P12]]
[[P2P]]
[[P7B]]

[[QoS]]

[[RA]]
[[RADIUS]]
[[RBAC]]
[[RCS]]
[[RFID]]

[[SAML]]
[[SDN]]
[[SED]]
[[SFTP]]
[[SMIME]]
[[SMS]]
[[SRTP]]
[[SSH]]
[[SSL]]
[[SSO]]
[[SWG]]

[[TACACS]]
[[TACACS+]]
[[TLS]]
[[TPM]]

[[UEFI]]
[[USB]]
[[USB_OTG]]
[[UTM]]

[[VDI]]
[[VLAN]]
[[VPC]]
[[VPN]]

[[WAF]]
[[Wi-Fi]]
[[WPA2]]
[[WPA3]]
