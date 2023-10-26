Sources:
https://resources.infosecinstitute.com/certification/the-security-cbk-domains-information-and-updates/
\
24% of the CompTIA SEC+ exam exam:
\
The first domain, Attacks, threats and vulnerabilities, deals with a basic need of every information security professional: being able to recognize and understand the different sources of threats, types of attacks and vulnerabilities that may be exploited. The SY0-601 focuses on issues related to today’s popular technology, including [[IoT]] and embedded devices, and the latest attack trends such as the newest [[DDoS]] attacks and sophisticated social engineering attempts.
\
Candidates must also know how to compare and contrast types of attacks. A wide array of issues need to be tackled, including tactics for social engineering, like [[Phishing]], [[Spear_Phishing]], [[Whaling]], [[Vishing]], [[Tailgating]] and [[Impersonation]]; application/service attacks, like [[DoS]]/[[DDoS]], [[Man-in-the-Middle]], [[Buffer_Overflow]], injection ([[SQL_Injection]]), [[Cross_Site_Scripting]], and privilege escalation ([[Local_Privilege_Escalation]]); wireless attacks, like [[Replay_Attacks]], [[Evil_Twin]], [[Rogue_AP]] and [[Jamming]]; and cryptographic attacks, such as [[Birthday_Attack]], known [[Plaintext]]/[[Cypher]] text, [[Rainbow_Tables]], [[Dictionary_Attack]]s, [[Brute_Force]], [[Hash_Collision]], [[Replay_Attacks]] and weak implementations.
\
It is also necessary to be able to explain concepts such as threat actor types and attributes. What is the difference between [[Hacktivist]]s and organized crime? How can [[Nation-State]]s be a threat? What level of sophistication should you expect from, and what are the differences in motivations, for insiders and external attackers? How can the use of [[Open_Source_Intelligence]] ([[OSINT]]) be implemented and help in creating a more effective cybersecurity strategy?
\
Testers are also expected to know the key concepts of penetration testing, including the different approaches ([[Black-Box]], [[White-Box]] and [[Gray-Box]] testing), and tactics ([[Active_Reconnaissance]], [[Passive_Reconnaissance]] and [[Escalation_of_Privilege]]).
\
Other concepts in this domain include explaining vulnerability scanning like passively testing security controls, how to identify vulnerabilities and intrusive vs. non-intrusive methods. It’s also important to know the impact associated with types of vulnerabilities such as [[Race_Condition]]s, improper input ([[Input_Escaping]], [[Input_Sanitization]], [[Input_Validation]]) and [[Error_Handling]], untrained users, memory/buffer vulnerabilities, architecture/design weaknesses, new threats/[[Zero-Day]], improper [[Certificate]] and [[PKI]] management.
# 1.0 Threats, Attacks, and Vulnerabilities

## **1.1 Compare and contrast different types of social engineering techniques:**

---

- [ ] [[Phishing]]
- [ ] [[Smishing]]
- [ ] [[Vishing]]
- [ ] [[Spam]]
- [ ] Spam over instant messaging ([[SPIM]])
- [ ] [[Spear_Phishing]]
- [ ] [[Dumpster_Diving]]
- [ ] [[Shoulder_Surfing]]
- [ ] [[Pharming]]
- [ ] [[Tailgating]]
- [ ] Eliciting information
- [ ] [[Whaling]]
- [ ] [[Prepending]]
- [ ] [[Identity_Fraud]]
- [ ] [[Invoice_Scams]]
- [ ] [[Credential_Harvesting]]
- [ ] [[Active_Reconnaissance]] / [[Passive_Reconnaissance]]
- [ ] Hoax
- [ ] [[Impersonation]]
- [ ] [[Watering_Hole_Attack]]
- [ ] [[Typosquatting]]
- [ ] [[Pretexting]]
- [ ] [[Influence_Campaign]]
- [ ] [[Hybrid_Warfare]]
	- [ ] -Social media
- [ ] [[Social_Engineering_Principles]] (reasons for effectiveness)
	- [ ] -Authority
	- [ ] -Intimidation
	- [ ] -Consensus
	- [ ] -Scarcity
	- [ ] -Familiarity
	- [ ] -Trust
	- [ ] -Urgency

## **1.2 Given a scenario, analyze potential indicators to determine the type of attack.**

---
- [ ] [[Malware]]
	- [ ] -[[Ransomware]]
	- [ ] -[[Trojan]]
	- [ ] -[[Worms]]
	- [ ] -Potentially unwanted programs ([[PUP]]s)
	- [ ] -[[Fileless_Virus]]
	- [ ] -[[Command_and_Control]] / [[C2]]
	- [ ] -[[Bots]]
	- [ ] -[[Cryptomalware]] [[Cryptographic_Attacks]]
	- [ ] -[[Logic_Bomb]]s
	- [ ] -[[Spyware]]
	- [ ] -[[Key_Logging]]
	- [ ] -[[Remote_Access_Trojan]] ([[RAT]])
	- [ ] -[[Rootkit]]
	- [ ] -[[Backdoor]]
- [ ] Password attacks
	- [ ] -[[Password_Spraying]]
	- [ ] -[[Dictionary_Attack]]
	- [ ] -[[Brute_Force]]
	- [ ] -Offline
	- [ ] -Online
	- [ ] -[[Rainbow_Tables]]
	- [ ] -[[Plaintext]]/unencrypted
- [ ] Physical attacks
	- [ ] -Malicious Universal Serial Bus ([[USB]]) cable ([[OMG_Cable]])
	- [ ] -Malicious flash drive ([[RubberDucky]])
	- [ ] -[[Card_Cloning]]
	- [ ] -[[Skimming]]
- [ ] [[Adversarial_Artificial_Intelligence]] ([[AI]])
	- [ ] -Tainted training data for machine learning ([[ML]])
	- [ ] -Security of [[Info_Sec_Studies/Sec+/Security+_Definitions/Machine_Learning_Algorithms]]
- [ ] [[Supply_Chain_Attacks]]
- [ ] [[Cloud]]-based vs. [[On-premise]]s attacks ([[Cloud]]/[[On-Premise]] Security)
- [ ] Cryptographic attacks
	- [ ] -[[Birthday_Attack]]
	- [ ] -[[Hash_Collision]]
	- [ ] -[[Downgrade_Attack]]

## 1.3 Given a scenario, analyze potential indicators associated with application attacks.

---
- [ ] • [[Local_Privilege_Escalation]]
- [ ] • Cross-site scripting ([[XSS]])
- [ ] • Injections
	- [ ] -Structured query language ([[SQL]]), ([[SQLi]])
	- [ ] -Dynamic-link library ([[DLL]])
	- [ ] -Lightweight Directory Access Protocol ([[LDAP]])
	- [ ] -Extensible Markup Language ([[XML]])
- [ ] • [[Pointer_Dereference]] / [[Object_Dereference]]
- [ ] • [[Directory_Traversal]]
- [ ] • [[Buffer_Overflow]]s
- [ ] • [[Race_Condition]]s
	- [ ] -Time of check/time of use ([[TOCTTOU]] attacks)
- [ ] • [[Error_Handling]]
- [ ] • [[Improper_Input_Handling]]
- [ ] • [[Replay_Attacks]]
	- [ ] -Session replays
- [ ] • [[Integer_Overflow]]
- [ ] • Request forgeries
	- [ ] -[[Server-side_Request_Forgery]]
	- [ ] -[[Cross-Site_Request_Forgery]] [[XSRF]]
- [ ] • Application programming interface ([[API]]) attacks
- [ ] • [[Resource_Exhaustion]]
- [ ] • [[Memory_Leak]]
- [ ] • Secure Sockets Layer stripping ([[SSL_Stripping]])
- [ ] • [[Driver_Manipulation]]
	- [ ] -[[Shimming]]
	- [ ] -[[Refactoring]]
- [ ] • [[Pass_the_Hash]]

## 1.4 Given a scenario, analyze potential indicators associated with network attacks.

---
- [ ] • Wireless
	- [ ] -[[Evil_Twin]] 
	- [ ] -[[Rogue_AP]]
	- [ ] -[[Bluesnarfing]]
	- [ ] -[[Bluejacking]]
	- [ ] -Disassociation ([[Deauth_Attack]])
	- [ ] -[[Jamming]]
	- [ ] -Radio frequency identification ([[RFID]])
	- [ ] -Near-field communication ([[NFC]])
	- [ ] -Initialization vector ([[IV]])
- [ ] • [[On-Path_Attack]] (previously known as [[Man-in-the-Middle]] attack/ [[Man-in-the-Browser]] attack)
- [ ] • Layer 2 attacks
	- [ ] -Address Resolution Protocol poisoning ([[ARP_Poisoning]])
	- [ ] -Media access control flooding ([[MAC_Flooding]])
	- [ ] -[[MAC_Cloning]]
- [ ] • Domain name system ([[DNS]])
	- [ ] -[[Domain_Hijacking]]
	- [ ] -[[DNS_Poisoning]]
	- [ ] -Uniform Resource Locator redirection ([[URL_Redirection]])
	- [ ] -[[Domain_Reputation_Attack]]
- [ ] • Distributed denial-of-service ([[DDoS]])
	- [ ] -[[Network]]
	- [ ] -Application
	- [ ] -Operational technology ([[OT]])
- [ ] • Malicious code or script execution
	- [ ] -[[PowerShell]]
	- [ ] -[[Python]]
	- [ ] -[[Bash]]
	- [ ] -[[Macro]]s
	- [ ] -Visual Basic for Applications ([[VBA]])

## 1.5 Explain different threat actors, vectors, and intelligence sources.

---
- [ ] • Actors and threats
	- [ ] -Advanced persistent threat ([[APT]])
	- [ ] -[[Insider_Threat]]s
	- [ ] -[[State_Actor]]s
	- [ ] -[[Hacktivist]]s
	- [ ] -[[Script_Kiddies]]
	- [ ] -[[Criminal_Syndicates]]
	- [ ] -Hackers
	- [ ] -Authorized
	- [ ] -Unauthorized
	- [ ] -Semi-authorized
	- [ ] -[[Shadow_IT]]
	- [ ] -Competitors
- [ ] • [[Attributes_of_Actors]]
	- [ ] -Internal/external
	- [ ] -Level of sophistication/capability
	- [ ] -Resources/funding
	- [ ] -Intent/motivation
- [ ] • Vectors
	- [ ] -Direct access
	- [ ] -Wireless
	- [ ] -Email
	- [ ] -[[Supply_Chain_Attacks]]
	- [ ] -Social media
	- [ ] -Removable media
	- [ ] -Cloud
- [ ] • Threat intelligence sources
	- [ ] -Open-source intelligence ([[OSINT]])
	- [ ] -Closed/proprietary
	- [ ] -[[Vulnerability_Databases]]
	- [ ] -Public/private information
	- [ ] -[[Sharing_Center]]s
	- [ ] -[[Dark_Web]]
	- [ ] -Indicators of compromise ([[IOC]])
	- [ ] -Automated Indicator Sharing ([[AIS]])
	- [ ] -Structured Threat Information eXpression ([[STIX]])/Trusted Automated eXchange of Intelligence Information ([[TAXII]])
	- [ ] -[[Predictive_Analysis]]
	- [ ] -[[Threat_Maps]]
	- [ ] -File/code repositories
- [ ] • Research sources
	- [ ] -Vendor websites
	- [ ] -[[Vulnerability_Feed]]s
	- [ ] -Conferences
	- [ ] -Academic journals
	- [ ] -Request for comments ([[RFC]])
	- [ ] -Local industry groups
	- [ ] -Social media
	- [ ] -[[Threat_Feed]]s
	- [ ] -Adversary tactics, techniques, and procedures ([[TTP]])

## 1.6 Explain the security concerns associated with various types of vulnerabilities.

---
- [ ] • [[Cloud-based_vs_On-Premises_Attacks]]
- [ ] • [[Zero-Day]]
- [ ] • Weak configurations
	- [ ] -Open permissions
	- [ ] -Unsecure [[Root]] account
	- [ ] -Errors
	- [ ] -Weak [[Encryption]]
	- [ ] -Unsecure Protocols
	- [ ] -Default settings
	- [ ] -Open [[Ports]] and [[Services]]
- [ ] • Third-party risks
	- [ ] -[[Vendor_Management]]
	- [ ] -System integration
	- [ ] -Lack of vendor support
	- [ ] -[[Supply_Chain_Attacks]]
	- [ ] -Outsourced code development
	- [ ] -Data storage
- [ ] • Improper or weak [[Patch_Management]]
	- [ ] -[[Firmware]]
	- [ ] -Operating system ([[OS]])
	- [ ] -Applications
- [ ] • [[Legacy_Platform]]s
- [ ] • Impacts
	- [ ] -[[Data_Loss]]
	- [ ] -[[Data_Breaches]]
	- [ ] -[[Data_Exfiltration]]
	- [ ] -[[Identity_Theft]]
	- [ ] -[[Financial_Impact]]
	- [ ] -[[Reputation_Impact]]
	- [ ] -[[Availability_Loss]]

## 1.7 Summarize the techniques used in security assessments.

---
- [ ] • Threat hunting
	-[[Intelligence_Fusion]]
	-[[Threat_Feed]]s
	-[[Advisories_and_Bulletins]]
	-Maneuver
- [ ] • Vulnerability scans
	-[[False_Positives_Vulnerability_Scan]]
	-[[False_Negatives_Vulnerability_Scan]]
	-[[Log_Review]]
	-[[Credentialed_Scan]] vs. [[Non-Credentialed_Scan]]
	-[[Intrusive_Vuln_Scan]] vs. [[Non-Intrusive_Vuln_Scan]]
	-[[Application_Vuln_Scans]]
	-[[Web_Application_Scan]]
	-[[Network_Vulnerability_Scan]]
	-Common Vulnerabilities and Exposures ([[CVE]])/Common Vulnerability Scoring System ([[CVSS]])
	-[[Configuration_Review]]
- [ ] • Syslog/Security information and event management ([[SIEM]])
	-[[Review_Reports]]
	-[[Packet_Capture]]
	-[[Data_Inputs]]
	-[[User_Behavior_Analysis]]

	-[[Sentiment_Analysis]]
	-[[Security_Monitoring]]
	-[[Log_Aggregation]]
	-[[Log_Collectors]]
- [ ] • Security orchestration, automation, and response ([[SOAR]])

## 1.8 Explain the techniques used in penetration testing.

---
- [ ] • Penetration testing
	- [ ] -[[Known_Environment]]
	- [ ] -[[Unknown_Environment]]
	- [ ] -[[Partially_Known_Environment]]
	- [ ] -[[Rules_of_Engagement]]
	- [ ] -[[Lateral_Movement]]
	- [ ] -[[Privilege_Escalation]]
	- [ ] -[[Persistence]]
	- [ ] -[[Cleanup]]
	- [ ] -[[Bug_Bounty]]
	- [ ] -[[Pivoting]]
- [ ] • [[Passive_Reconnaissance]] and [[Active_Reconnaissance]]
	-[[Drones]]
	-[[War_Flying]]
	-[[War_Driving]]
	-[[Footprinting]]
	-[[OSINT]]
- [ ] • Exercise types
	-[[Red-Team]]
	-[[Blue-Team]]
	-[[White-Team]]
	-[[Purple-Team]]

---


# Acronyms used in this domain of the exam:

---

[[AI]]
[[AIS]]
[[API]]
[[AP]]
[[APT]]
[[ARP]]
[[AV]]

[[CSRF]]
[[CVE]]
[[CVSS]]

[[DDoS]]
[[DLL]]
[[DNS]]

[[IOT]]
[[IV]]

[[MAC]]
[[ML]]

[[NFC]]

[[OS]]
[[OSINT]]
[[OT]]

[[PKI]]
[[PUP]]

[[RAT]]
[[RFC]]
[[RFID]]

[[SIEM]]
[[SOAR]]
[[SSL]]
[[STIX]]
[[SPIM]]
[[SQL]]
[[SQLi]]

[[TAXII]]
[[TOCTTOU]]
[[TTP]]

[[USB]]

[[VBA]]

[[XML]]
[[XSS]]
[[XSRF]]