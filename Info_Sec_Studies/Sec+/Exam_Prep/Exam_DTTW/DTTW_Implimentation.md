# Q1:
You are in the process of adding access control list (ACL) rules to a stateless firewall. The goal is to ensure that any traffic that is not explicitly allowed by one of the rules is implicitly denied.

Where should the deny all rule be placed within the access control lists?

What did I answer?:
**The implicit deny rule should be the first rule in an ACL**

Correct answer: **The implicit deny rule should be the last rule in an ACL**

The implicit deny rule should be the last rule listed within an access control list (ACL). Configured in this way, the firewall will compare the traffic against all of the rules first, and if it doesn't meet the requirements of those rules, it will be denied by the final rule.

If the implicit deny rule is listed first, it will deny all traffic without comparing the traffic against the allow rules that follow. Placing it in the middle of the ACL would cause the same issue as placing it first; any rules listed after the implicit deny rule would be ignored.

# Q2:
A network engineer has been tasked with configuring a virtual private network (VPN) between a company's Texas location and the company's California location.

Which type of tunnel should the network engineer implement?

What did I answer?:
**Remote access**

Correct answer: **Site-to-site**

A site-to-site virtual private network (VPN) tunnel is used to connect to networks that are geographically separated. Site-to-site VPNs allow for the connection of both networks without requiring additional steps on the user's part.

A remote access VPN allows the user to connect directly from their laptop using a VPN software client to connect to a VPN gateway. This is often implemented for traveling or remote users to connect to the corporate network. A flood guard and round-robin are not types of VPN tunnels.

# Q3:
You are researching biometric systems for your organization.

Which of the following indicates that a biometric system is more accurate?

What did I answer?:
**A higher CRR**

Correct answer: **A lower CER**

CER refers to a biometrics crossover error rate. The crossover error rate (CER) is calculated by plotting the false acceptance rate (FAR) and false rejection rate (FRR). The point where the FRR and FAR meet is the CER. If you are evaluating multiple biometrics systems, the one with the lowest CER is the most accurate.

The acronym CRR is fabricated for this question.

# Q4:
Correct answer: NTLM

New Technology LAN Manager (NTLM) is the least secure of the options given. NTLM creates an MD4 hash of a user's password. Since MD4 can be cracked, NTLM shouldn't be used. NTLMv2 and NTLM2 are two more secure versions of NTLM, but Microsoft still recommends not using any of these authentication services.

Kerberos, Lightweight Directory Access Service (LDAP), and Lightweight Directory Access Services Secure (LDAPS) are all more secure than NTLM.

What did I answer?:
**LDAP**

Correct answer: **NTLM**

New Technology LAN Manager (NTLM) is the least secure of the options given. NTLM creates an MD4 hash of a user's password. Since MD4 can be cracked, NTLM shouldn't be used. NTLMv2 and NTLM2 are two more secure versions of NTLM, but Microsoft still recommends not using any of these authentication services.

Kerberos, Lightweight Directory Access Service (LDAP), and Lightweight Directory Access Services Secure (LDAPS) are all more secure than NTLM.

# Q5:

You are interested in isolating a corporate application on your mobile device away from all personal items on that device. You'd also like that application and all of the data associated with it to be encrypted but aren't interested in encrypting the entire device.

Which of the following is the BEST solution for this scenario?

What did I answer?:
**Sideloading**

Correct answer: **Containerization**

Containerization is the process of running an application in a container, isolated from the rest of the data on the device. By running the application inside of a container, that container can be encrypted and the data is protected from the rest of the items on the device.

# Q6:
A security engineer has placed an intrusion detection system (IDS) in the cloud. Traffic doesn't pass directly through the IDS but is forwarded to the IDS after it has entered the network. As such, the IDS would be able to alert after an intrusion has occurred, but not before.

What is this known as?

What did I answer?:
**Inline**

Correct answer: **Out-of-band**

Out-of-band, also known as passive, means that the device monitors network traffic, but traffic doesn't have to go through the device.

Inline, or in-band, devices are devices that traffic must go through to enter the network. An intrusion prevention system (IPS) would be inline, and as that traffic passes through the IPS, it can prevent malicious traffic before it enters the network. The term outward doesn't apply to the question.

# Q7:
A user tries to open a certificate file, but is asked for a password.

Which type of certificate are they trying to open?

What did I answer?:
**PEM**

Correct answer: **PFX**

The Personal Information Exchange (PFX) format is a binary file used often in Windows environments. It encrypts all the data inside and needs a password to be opened.

---

# Study
Below are questions I had flagged in my practice exams but got correct, Write out why I would be unsure about what the answer is and the correct answer in my own words that makes sense to me.

---

In IPSec, which of the following encrypts data and provides confidentiality?

Correct answer: ESP

IPSec provides security in two ways: ESP and AH. Encapsulating Security Payload (ESP) is used to provide encryption of data and provide confidentiality.

Authentication Header (AH) allows each of the hosts in the IPSec communication to authenticate with each other before exchanging data. AH provides authentication and integrity. TLM and DNP are fabricated terms.

---

You are setting up multifactor authentication (MFA) for an account. It is asking you to use a "something you are" authentication factor.

Which of the following could be used to meet the "something you are" authentication factor?

Correct answer: Biometrics

The "something you are" authentication type refers to biometrics. This could include items such as fingerprint scanners, retina scanners, iris scanners, and any other method that uses a part of your body.

A PIN is considered "something you know." Hardware tokens and ID cards are both considered "something you have".

---

You are working as a systems administrator for an organization and find that many users have trouble remembering multiple passwords to log into all company systems. You would like to implement a system in which users can log into multiple systems by entering their password once.

What should you implement to achieve this?

Correct answer: SSO

Single sign-on (SSO) allows a user to log into multiple systems or programs after successfully entering their credentials only once. For example, a user can enter a single strong domain password to access company email, file servers, ticketing systems, payroll websites, and more. Single sign-on allows a user to create one strong password that they can remember rather than remember many passwords. This increases security because users will often write down passwords if they have to remember too many.

Multi-factor authentication (MFA) requires that users have two or more types of authentication methods to access a system. MFA can–and should–be implemented on top of SSO to add extra security. A security information and event management (SIEM) solution is used to correlate and aggregate logs from various systems. File Transfer Protocol (FTP) is a protocol used to transfer files over a network.

---

Of the two IPSec modes, which mode encrypts the entire IP packet rather than just the packet's payload?

Correct answer: Tunnel mode

The two modes associated with IPSec are tunnel mode and transport mode. Tunnel mode encrypts the entire IP packet, and transport mode only encrypts the packet's payload. Tunnel mode is used with VPNs transmitted over the internet, and transport mode is often used in private networks.

Light mode and authentication mode are not types of IPSec modes.

---

You are working for an organization that relies heavily on the use of mobile devices. Specifically, employee mobile phones contain a lot of confidential data that could be damaging if the device ends up in the wrong hands. You are implementing security controls that would help reduce the damage caused in the event of loss or theft.

Of the following, which would NOT make sense to implement to achieve this goal?

Correct answer: Jailbreaking

Jailbreaking is the process of removing carrier or manufacturer restrictions from a mobile device. Jailbreaking poses a risk because any of the protections built into the device by default are no longer in place after the jailbreak has occurred.

Screen locks, remote wiping, and FDE (full device encryption) are all practices that could help prevent damage if a device was lost or stolen.

---

Ana, Mark, and Zoe use the same computer. Ana created a folder on the computer named "Office Admin Files". She has determined that Mark will need access to these files, but not Zoe. Ana configures the permissions so that Mark can access the folder when he's on that computer, but Zoe cannot.

What type of access control method is in place in this scenario?

Correct answer: DAC

Discretionary Access Control (DAC) is an access control method in which the owner of an object (such as a file, folder, printer, etc) determines who can access the object. Ana is the owner of the object (the folder) in this scenario and has decided, based on her own discretion, that Mark should have access to that object and not Zoe.

---

A user has approached you and asked about file transfers. He would like to know which protocol is not secure enough to transfer confidential data.

Of the following, which protocol is NOT a secure method for transferring files?

Correct answer: FTP

File Transfer Protocol (FTP) operates on ports 20 and 21. FTP transmits data in cleartext by default, making it an insecure protocol to use for file transfer. File Transfer Protocol Secure (FTPS) is an extension of the FTP protocol that uses Transport Layer Security (TLS) to encrypt FTP traffic, making it a more secure solution.

Secure File Transfer Protocol (SFTP) uses Secure Shell (SSH) to transmit files in an encrypted manner. It can be easy to confuse FTPS and SFTP, but they operate differently. Secure Copy Protocol (SCP) uses SSH and is used to copy encrypted files over a network.

---

Windows domains use Active Directory (AD).

Which of the following protocols is AD based on?

Correct answer: LDAP

Windows domains use Active Directory (AD), which is based on Lightweight Directory Access Protocol (LDAP). LDAP operates at the application layer and is used for accessing and altering directory services data.

---

What is the MOST commonly used protocol for time synchronization?

Correct answer: NTP

Network Time Protocol (NTP) is the most commonly used protocol for time synchronization.

Simple Network Time Protocol (SNTP) may not be as accurate as NTP and therefore, is not used as commonly. Kerberos and SMTP are not time synchronization protocols. Kerberos is an authentication protocol. SMTP is the Secure Mail Transfer Protocol (SMTP).

---

Before installing a new patch for a piece of software, engineers would like to test it inside an isolated environment to analyze the impact of the patch.

What is the term used to describe an isolated environment used for testing?

Correct answer: Sandbox

A sandbox is an isolated system that is often used for testing. Sandboxing is regularly used by malware analysts to run malware in an isolated environment and see how it behaves. Additionally, sandboxing can be used by administrators to test patches and updates before installing them company-wide. Software developers may also use sandboxing to test their own programs.

The term white box is used to describe a penetration test in which the tester has full knowledge of the entire network or systems. Honeypots are decoy systems used to distract and trick attackers into thinking it is a legitimate system. A honeynet is a network or part of a network that contains multiple honeypots.

---

You are working as a security engineer for a web application developer. You have been tasked with reducing the chance of a cross-site scripting (XSS) attack against a web application.

Which of the following is the BEST way to reduce the possibility of XSS?

Correct answer: Input validation

Cross-site scripting (XSS) is a type of injection attack. Injection attacks occur when a flaw or bug in an application is exploited by inserting (or injecting) invalid information into the application. The best way to combat an XSS attack is to use input validation to ensure that anything entered into the application is valid and non-malicious.

---

A woman posted a photo on social media that showed herself and her friends. She did not share any information about her location, and the photo didn't show anything that would indicate she was out of town. However, a thief saw her photo and determined that she was out of the state. Knowing that she was out of town, he targeted her home for a burglary.

If there wasn't any information in her social media post about where she was, and the photo didn't contain any evidence of being out of town, how could the thief know where she was?

Correct answer: Geotagging

GPS tagging, or geotagging, is the process in which geographical information is added to photos when they are uploaded to the internet, such as on social media websites. By viewing this information on photos, an attacker could essentially determine when they are at home and when they are away. This is particularly useful for thieves trying to find time to burglarize a home without their victims being there.

---

You are a network engineer implementing a new packet filtering firewall. The firewall could be considered a pure packet filtering firewall as it does not store the packets but simply inspects each one and allows or denies it based upon predefined rules.

What type of firewall is being implemented?

Correct answer: Stateless firewall

A stateless firewall is a type of packet filtering firewall. Stateless firewalls are considered pure packet filtering firewalls because, unlike stateful firewalls, they do not retain the memory of the packets that have passed through. Instead, they simply inspect the packets and allow or deny them based upon the pre-defined rules.

---

You are working as a network engineer and implementing a new firewall. The firewall inspects traffic and is capable of making decisions based upon that traffic. For example, if the device detects transmission control protocol (TCP) traffic without a corresponding three-way-handshake, it blocks that traffic because it is deemed as suspicious behavior.

What type of firewall is being implemented?

Correct answer: Stateful firewall

A stateful firewall inspects traffic and makes decisions based upon the state of the traffic. Stateful firewalls keep track of established sessions and block traffic that isn't a part of an established session.

This is different from a stateless firewall, which doesn't keep track of sessions and relies solely on access control lists (ACLs) for decisions on blocking and allowing traffic. Windows firewall and iptables are both personal firewalls (PFs) and are not capable of performing the type of inspection described in the scenario.

---

