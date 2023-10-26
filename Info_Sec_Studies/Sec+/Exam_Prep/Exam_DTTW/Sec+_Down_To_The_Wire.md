
Actually Useful Shit:
[[Cert_Master_Wrong_Answers]]


## These are all from the IT and Security study app for Sec+:

- [[DTTW_Architecture_and_Design]]
- [[DTTW_Implimentation]]
- [[DTTW_GRC]]
- [[DTTW_Attacks_Threat_Vulns]]

---

## These are all from CompTIA Sec+ Cert master:

**Implementation:**
---

Two employees use [[IM]] in separate buildings at work. They change the communications over to a voice call with one click. Compare the types of communication services and determine which service the employees used. 
\
I answered Video teleconferencing but the answer is [[Unified_Communications]].
\
Unified comms is the correct answer because of the fact that the employees were using IM and they didn't have to change the app to pull up a video call and were able to use the same app for both purposes. Unified comms is tools like Microsoft Teams or G Suite where you can be sending emails and a power point document with someone and then call them on google meet without ever having to leave the app.
\
The project managers are utilizing [[Unified_Communications]]. These solutions are messaging applications that combine multiple communications channels and technologies into a single platform. These communications channels can include voice, messaging, interactive whiteboards, data sharing, email, and social media.
\
Voice over internet protocol [[VOIP]] is a type of voice communication. While this could have been utilized for the first portion of the communication, it could not have been utilize3d without additional tools to change to video.
\
[[Video_Teleconferencing]] is for voice and video. The project managers started on a voice-only call, therefore, this was not the solution they were using.
\
Web conferencing is for live meetings. The call started as voice-only, and is not applicable for this scenario.

---

A systems admin deploys a new infrastructure for an organization. Examine the given descriptions and determine which applies to the technology used with the [[LDAP]] protocol.
\
I answered Forward traffic from one node to another, but the answer is Provides privilege management and authorization.
\

\
Directory services are the principal means of providing privilege management and authorization on an enterprise network. The lightweight directory access protocol ([[LDAP]]) is a protocol used with X.500 format directories.
\
The Dynamic Host Configuration Protocol ([[DHCP]]) provides an automatic method for network address allocation. Only one server should be offering addresses to any one group of hosts.
\
The basic function of a network is to forward traffic from one node to another. Several routing and switching protocols are used to implement forwarding with layer 2 and 3 devices.
\
The domain name system (DNS) resolves fully qualified domain names ([[FQDN]]s) to IP addresses. It uses a distributed database system that contains information on domains and hosts within those domains.

---

A company provides smartphones to their employees. IT administrators have the ability to deploy, secure, and remove specific applications and data from the employees' smartphones. Analyze the selections and determine how IT can perform this type of control.
\
Storage segmentation is personal data segmented from organizational data on a mobile device. It gives IT administrators control over corporate assets on employees' mobile devices.
\
A content management system tags corporate or confidential data and prevents it from being shared or copied to unauthorized media or channels, such as non-corporate email systems or cloud storage services.
\
A baseband update modifies the firmware of the radio modem used for cellular, Wi-Fi, Bluetooth, NFC, and GPS connectivity.
\
Push notifications are store services (such as Apple Push Notification Service and Google Cloud to Device Messaging) that an app or website can use to display an alert on a mobile device.

---

A zone separated from the local network, provides business partners access to company resources without disclosing internal information. What type of zone does this illustrate?
\
I answered DMZ but the answer is Extranet.
\
An extranet is a zone created to allow authorized users access to company assets separate from the intranet.
\
An intranet is an internal company zone established to allow employees the ability to share content and communicate more effectively.
\
A Demilitarized Zone (DMZ) is an area of a network that is designed specifically for public users to access. The DMZ is a buffer network between the public untrusted internet and private trusted LAN.
\
A Virtual Local Area Netw ork (VLAN) is a logical group of network devices on the same LAN, despite their geographical distribution. It can divide the devices logically on the data link layer, and group users according to departments.

---

WPA (Wi-Fi Protected Access) fixes the security problems with WEP (Wired Equivalent Privacy) by adding TKIP (Temporal Key Integrity Protocol) to the RC4 cipher to make it stronger. TKIP fixes the checksum problem, uses a larger initialization vector (IV), transmits it as an encrypted hash, and adds a sequence counter to resist replay attacks. What replaced RC4/TKIP to make WPA2 significantly more secure than WPA?
\
I answered AES/IEEE 802.1x, but the answer was AES/CCMP.
\
For WPA2, AES (Advanced Encryption standard) deploys within CCMP (Counter Mode with Cipher Block Chaining Message Authentication Code Protocol). AES replaces RC4, and CCMP replaces TKIP. AES is for encryption, and CCMP is for message integrity.
\
IEEE 802.1x is a standard for encapsulating EAP (Extensible Authentication Protocol) communications over a LAN or WLAN. WPA2-Enterprise uses this standard.
\
SHA-2 (Secure Hashing Algorithm 2) is a hashing algorithm, not an encryption method. It is widely implemented as part of security standards and protocols, such as SSL, IPsec, and Digital Signature Standards (DSS).
\
IEEE 802.1x, which is a Port-Based Network Access Control (PNAC) does not provide message integrity. SHA-2 has no purpose with 802.1x.

---

Which of the following will reduce the risk of data exposure between containers on a cloud platform?
\
I answered Control groups, but the answer was Control groups, and Namespaces.
\
In a container engine such as Docker, each container is isolated from others through separate namespaces. Namespaces prevent one container from reading or writing processes in another.
\
Control groups ensure that one container cannot overwhelm others in a DoS-type attack. Namespaces and control groups reduce the risk of data exposure between containers.
\
Public subnets allow a service or even container in the cloud to connect directly with an internet gateway. Although this does pose some security risk, these public subnets assist primarily with connectivity to and from external resources.
\
Secrets management is the management of credentials specific for running or accessing service on a cloud service provider. This includes implementing multi-factor authentication (MFA) for interactive logons.

---

A network administrator sets up a stateless firewall using an open-source application running on a Linux virtual machine. The immediate benefit of this setup is that it was easy to set up quickly with basic rules. What other reasons may have influenced the administrator's decision to deploy a stateless rather than a stateful firewall?
\
I answered Allow network protocols, and hardware performance but the right answers were Allow network protocols, and Block TCP ports.
\
A packet filtering firewall is configured by specifying an access control list (ACL). An ACL may define port filtering or security rules to block, for example, TCP port 3389 which is used for remote desktop protocols.
\
A packet filtering firewall may also set rules for protocol ID or type. For example, it may allow HTTPS traffic.
\
Hardware or physical firewalls are great for performance because the hardware is specific to the job. In this case, a virtual appliance firewall was deployed.
\
A stateful inspection firewall can analyze, for example, HTTP headers and the HTML code present in the HTTP packets to identify code that matches patterns in a threat database. A web application firewall (WAF) is a stateful inspection firewall.

---

A network engineer is plugging in new patch cables and wants to prevent inadvertent disruptions to the network while doing so. What will the engineer prevent if a Spanning Tree Protocol (STP) is configured on the switches?
\
I answered MAC floods, but the answer is Broadcast storms.
\
A spanning tree protocol (STP) is a means for bridges to organize themselves into a hierarchy and prevent loops from forming. These loops have the potential for broadcasting multiple times creating a storm.
\
Media access control (MAC) filtering guard against MAC flooding attacks. This filtering sets a limit to the number of permitted MAC addresses on a port. The port disabled once the limit is reached.
\
Dynamic host configuration protocol (DHCP) snooping is a network configuration setting that inspects this traffic on access ports to ensure that a host is not trying to spoof its MAC address.
\
Network intrusion prevention systems provide an active response to any network threats that it matched to signatures and even heuristic behavior patterns.

---

Network administrators are configuring a demilitarized zone (DMZ) to provide Internet-facing services to customers. These admins will perform minimum configuration and security to rapidly deploy two web servers that are load balanced. Which of the following will most likely be configured in this DMZ?
\
I answered Virtual Up addresses, and Zero trust, but the answers were, Virtual IP addresses, Scheduling algorithm, and Bastion hosts.
\
Bastion hosts are any servers that are configured with minimal service to run in a demilitarized zone (DMZ). A bastion host would not be configured with any data that could be a security risk to the internal network.
\
Virtual Internet Protocol (IP) addresses are public IP addresses that are shared among a load-balanced cluster of servers. The primary node will receive traffic from the virtual IP address until the secondary node takes over.
\
The scheduling algorithm is the code and metrics that determine which node is selected for processing each incoming request. For example, round robin.
\
Zero trust is an advanced perimeter setup that uses continuous authentication and conditional access to mitigate privilege escalation and account compromise by threat actors.

---

Two companies are planning to provide their users with easier access to wireless access points at any of the company locations using personal company credentials. The companies will use Extensible Authentication Protocol (EAP) so that users are not required to memorize more passwords. How would a network administrator set up such a wireless network for these users?
\
I chose the answer create a Demilitarized zone, but the answer is Create a RADIUS federation.
\
RADIUS federation means that multiple organizations allow access to one another's users by joining their RADIUS servers into a RADIUS hierarchy or mesh.
\
Replacing the RADIUS solutions with Terminal Access Controller Access-Control System Plus (TACACS+) is not feasible. TACACS+ usually manages switches and routers.
\
Deploying new domain controllers will not benefit the requirement. The domain controllers for each company will remain as is and the RADIUS clients can route user credentials to the appropriate RADIUS servers.
\
Creating a Demilitarized Zone (DMZ) for these RADIUS servers is not an ideal setup. RADIUS servers will remain at the internal LANs and are only accessed by the RADIUS clients or wireless access points when necessary.

---

A web administrator notices a few security vulnerabilities that must be addressed on the company Intranet. The portal must force a secure browsing connection, mitigate script injection, and prevent caching on shared client devices. Determine the secure options to set on the web server's response headers.
\
I answered Cache-Control but the answers were Cache-control, Content Security Policy (CSP), and HTTP Strict Transport Security (HSTS)
\
HTTP Strict Transport Security (HSTS) is a header option that forces the browser to connect using HTTPS only, mitigating downgrade attacks, such as SSL stripping.
\
Content Security Policy (CSP) is a header option that mitigates clickjacking, script injection, and other client-side attacks.
\
Cache-Control is a header option that sets whether the browser can cache responses. Preventing data caching protects confidential and personal information where the client device is shared by multiple users.
\
Secure cookies mitigate the vector of session hijacking and data exposure. Cookies are made secure with key parameters for the SetCookie header that can, for example, only allow cookies to be used for HTTP.

---

A company is looking into integrating on-premise services and cloud services with a cloud service provider (CSP) using an Infrastructure as a Service (IaaS) plan. As a cloud architect works on architectural design, which of the following statements would NOT apply in this case?
\
I answered The company must establish separation of duties mechanisms, but the answer is The provider is responsible for the availability of the software.
\
In a Software as a Service (SaaS) plan, the provider is responsible for the availability of the software. The software may include an appliance with Windows Server 2016 already installed and available to use.
\
In an infrastructure as a Service (IaaS) plan, the provider is responsible for physical server. This responsibility includes updating firmware and even security patches.
\
The company that gathered customer data is responsible for legal and regulatory tasks required to process and ensure customer privacy. Cloud service providers (CSP) are responsible for the underlying storage that the data is hosted on.
\
The company is responsible for effective security mechanisms like separation of duties. For example, an Identity Access Management service can secure permissions to cloud storage.

---

**Governance, Risk, and Compliance:**
---

After reading an article online, a business stakeholder is concerned about a risk associated with DoS attacks. The stakeholder requests information about what countermeasures would be taken during an attack. Where would the security analyst look to find this information?
\
I answered Risk and Control Assessment but the answer is Risk Register.
\
The risk register shows the results of risk assessments in a comprehensible document format. Information in the register includes impact, likelihood ratings, date of identification, description, countermeasures, owner/route for escalation, and status.
\
The risk heatmap is a graphical table indicating the likelihood and impact of risk factors identified for a workflow, project, or department for reference by stakeholders. The heatmap alone does not include countermeasures.
\
Regulations affect risk posture but do not include specifics related to specific risks or a company. Regulations include requirements to deploy security controls and make demonstrable efforts to reduce risk.
\
Risk and control assessment is a process that identifies risks and assess the effectiveness of the controls intended to mitigate those risks. This process does not define countermeasures used after a risk is realized.

---

An employee at a financial firm is responsible for ensuring that data is stored in accordance with applicable laws and regulations. What role does the employee have in terms of data governance?
\
I answered Data custodian but the answer is Data Steward.
\
The data steward is primarily responsible for data quality. This involves tasks such as ensuring data is labeled and identified with appropriate metadata, as well as ensuring the data is collected and stored in a format containing values that comply with applicable laws and regulations.
\
The owner is responsible for labeling the asset and ensuring that it is protected with appropriate controls.
\
The data custodian handles managing the system on which the data assets are stored.
\
The data processor is the entity engaged by the data controller to assist with technical collection, storage, or analysis tasks.

---

An organization that is planning a move to the cloud checks to see that the chosen CSP uses a standard method for creating and following security competencies. Which method does the CSP likely implement?
\
I answered Service Organization Control (SOC2) but the answer is Cloud Controls matrix.
\
Cloud controls consists of specific controls and assessment guidelines that should be implemented by CSPs. A matrix acts as a starting point for agreements as it provides a baseline level of security competency that the CSP should meet.
\
Data Enterprise reference architecture is a best practice methodology and tools for CSPs to use in architecting cloud solutions.
\
Laws pertain to data compliance issues. Laws can be complicated by the fact that they derive from difference sources, such as localities and countries.
\
Service Organization control (SOC2) evaluates the internal controls implemented by the service provider to ensure compliance with trust services criteria (TSC) when storing and processing customer data.

---

In a particular workplace, all user actions are recorded and accounted for. Any time a resource is updated, archived, or a user has their clearance level changed, it must be approved by a root user. Users that leave, arrive, or change jobs (roles) must have their user accounts regularly recertified, and any account changes must be approved by an administrator. What are these measures known as?
\
I answered Separation of duties but the answer is change control.
\
change control of quality management systems and information technology systems is a process used to ensure that changes to the product or system are implemented in a managed and organized matter.
\
Separation of duties is a way of maintaining checks and balances against the risk that sensitive process or practices can be disrupted by insider attacks. Duties and responsibilities should be shared between people to avoid ethical conflict or misuse of powers.
\
Job rotation (or rotation of duties) ensures that no one is able to continue working in the same job for an extended amount of time.
\
An acceptable use policy is a collection of rules that are enforced by the network, website or service owner, developer or administrator, restrings the ways in which the network, platform or device should be sued and setting limits for how it can be used.

---

A group of junior systems administrators participates in an ethical hacking seminar that allows for advancement and rewards for completing challenges. Which training methods do the administrators experience?
\
I answered Gamification and Role-based training and the correct answers were Gamification and Capture the flag.
\
Ethical hacker training programs and gamified competitions usually use Capture the Flag (CTF). Participants must complete a series of challenges that usually result in identifying a threat actor (the flag).
\
Gamification is a learning approach that includes a fun-factor and features gaming type elements such as points, leveling up, and rewards.
\
A phishing campaign training event means sending simulated phishing messages to users. users responding to the messages can be targeted for follow-up training.
\
Appropriate security awareness training needs to be delivered to employees at all levels, including end-users, technical staff, and executives. This training often includes role-playing activities.

---

How does the General Data Protection Regulations (GDPR) classify data that can prejudice decisions, such as sexual orientation?
\
I answered Private, but the answer is Sensitive.
\
The sensitive classification is used in the context of personal data about a subject that could harm them if made public and could prejudice decisions made about them if referred to by internal procedures.
\
Private data is information that relates to an individual identity. An example of private data can be information, such as an identification number.
\
Proprietary information is created and owned by the company, typically about the products or services that they make or perform.
\
Confidential information is highly sensitive, for viewing only by approved persons within the owner organization.

---

**Architecture and Design:**
---

A cloud service provider (CSP) offers an organization the ability to build and run applications and services without having to manager infrastructure such as provisioning, authentication, and service maintenance. This offering reduces overhead and allows the organization to focus on the product being built. What type of design pattern is this?
\
I answered software defined network, but the answer is Serverless architecture.
\
A serverless architecture is a cloud model where applications are hosted by a third-party provider. A serverless architecture removes the responsibility of the consumer to provision, scale, and maintain server and storage solutions by applying functions and microservices.
\
A microservice architecture structures an application as a collection of services that are independent of one another and structured around business capabilities.
\
A service oriented architecture (SOA) Allows services to communicate with each other across different platforms and languages by implementing loose coupling technologies.
\
A software defined network (SDN) separates the data and control planes of a network by using software and virtualization technologies.

---

A system administrator implements a process that provides two separate paths from each server node to every disk in a redundant array of inexpensive disks set up to remove a single point of failure. What concept has the administrator implemented?
\
I answered Fault Tolerance, but the answer was Multipathing.
\
Multipathing allows users to configure multiple input/output (I/O) paths between server nodes and storage arrays into a single device to remove a single point of failure and increase redundancy.
\
The longevity of a cryptographic key is determined by the amount of data or number of uses and the sensitivity of the data. As the sensitivity of data being protected by cryptography keys increases, the longevity of the key should decrease.
\
Load balancing utilizes multiple servers to support a single service to increase system availability.
\
Fault tolerance is the ability of a system to suffer a defect and continue to operate as normal.

---

A cyber security team would like to gather information regarding what type of attacks are occurring on a network. Which of the following implementations would assist in routing information on the attackers to a Honeynet?
\
I answered honeypot, but the answer is DNS sinkhole.
\
Domain Name SErvice (DNS) sinkhole is used to intercept DNS requests attempting to connect to known malicious or unwanted domains and returning a fake IP address.
\
A honeypot is a server that is intentionally left open or available so that an attacker will be drawn to it versus a live network.
\
Distributed denial of service (DDoS) blackhole routing is a countermeasure to mitigate a DDoS attack in which network traffic is routed into a nothing space and lost.
\
Spear phishing is a targeted form of phishing in which an email is sent to a specific group of users to obtain personal information.

---

A security administrator protects systems passwords by hashing their related keys. The administrator discovers that this approach does not make the key any stronger or more difficult to crack. Analyze the different security properties and determine which one the administrator implemented.
\
I answered Digital signatures, but the answer was Key stretching.
\
Key stretching takes a key that is generated from a user password and repeatedly convers it to a longer and more random key.
\
The range of key values available to use with a particular cipher is called the keyspace. Using a longer key (256 bits rather than 128 bits, for instance) makes the encryption scheme stronger.
\
Digital signatures combine public key cryptography with hashing algorithms to provide authentication, integrity, and non-repudiation.
\
With key exchange, a symmetric encryption key is encrypted by the client and sent to the server. The server decrypts the key and that secret key is then used to encrypt messages sent between server client.

---

Devices deployed in a network and that send data to the local area network (LAN) level and process it with an Internet of things (IoT) sensor are which of the following?
\
I answered Edge computing but the answer is Fog computing.
\
Fog computing provides decentralized local access by deploying fog nodes throughout the network. Fog computing analyzes data on the network edge to avoid the need to transfer unnecessary data back to the LAN.
\
Edge computing is a distributed model that is accomplished at or near the source of the data where it is needed. These devices perform early processing of data to and from edge devices to enable prioritization.
\
In cloud computing, a company uses a cloud service provider to deliver computing resources. A cloud-based server utilizes virtual technology to host a company's applications offsite.
\
On-premise computing refers to a company's infrastructure and resources being maintained locally in the company. The company is responsible for managing and maintaining assets.

---

In which environment can multiple developers check out software code and include change management processes?
\
I answered staging but the answer is Development.
\
A development environment is where developers create a product. Developers check out code for editing or updating. Version control and change management occur in the development environment to track development.
\
A production environment mimics that of a production environment. It is used for dynamic analysis of an application in a complete but separate production-like environment.
\
A test environment does not fully simulate a production environment. The test environment allows for vulnerability scanning, penetration testing. and function user testing before being deployed to the staging environment.

---

A user receives access to a company system through the use of a smart card. The user can then access data they have privileges to access. A record of all events the user accomplishes or attempts to is recorded in a log for administrative purposes. What access management policy does this best describe?
\
I answered MAC, but the answer is AAA.
\
Authentication, Authorization, and Accounting (AAA) provides a comprehensive access management approach to identifying, authorizing, and accounting for user activity.
\
Group based access control is a role-based access control model that assigns privileges to a group and then adds users to a group.
\
A mandatory access control (MAC) uses security labels to determine access levels of a user. MAC is used when access should be restricted based on a "need to know."
\
A discretionary access control (DAC) model assigns an owner to an object, and the owner establishes access to users for the objects.

---

A test team performs an in-depth review of completed code and analyzes its compatibility with the environment it will be deployed to. Which of the following environments is the test occurring in?
\
I answered Development, but the answer is Staging.
\
A staging environment mimics that of a production environment. It is used for dynamic analysis of an application in a complete but separate production-like environment.
\
A test environment does not fully simulate a production environment. The test environment allows for vulnerability scanning, penetration testing, and function user testing before being deployed to the staging environment.
\
A production environment is where the final product is placed. All testing and development are complete at this point.
\
A development environment is where developers create a product. Developers check out code for editing or updating.

---

Differential, full, and incremental refer to which of the following when discussing backup types that will not collect open files?
\
I answered Snapshot, but the right answer is Copy.
\
A copy-based backup is a replica of an IT system. A copy of a system can be performed at any time to provide a system a means of backup. Copy-based backups will not copy open files.
\
A snapshot is a point-in-time copy of data in a system. A system administrator can select a certain point in time to create a snapshot. A snapshot will copy open files.
\
An image backup is a duplication of an operating system installation. An image allows quick redeployment without having to reinstall third-party software, patches, and changing configuration settings. An image does not contain users files.
\
A storage area network (SAN) solution provides access to block-level data storage that can be access by multiple users.

---

A database export allows personally identifiable information (PII) to display in report format and on screen. This poses a potential data leakage concern. In order to protect this PII, what de-identification method should the programmer consider implementing?
\
I answered Tokenization, but the answer is Data masking.
\
Data masking is a secure coding technique used to hide sensitive or private data from disclosure. All or part of the data fields are altered by substituting character strings with a random character.
\
Tokenization is a database de-identification method where all or part of data in a field is substituted with a randomly generated token. The token is stored with the original value separate to the production database.
\
Hashing is a cryptographic process that creates a fixed length string from an input plaintext. Hashes are created at separate times to verify integrity of a file.
\
Salting is the process of creating and adding random data as a secondary input to one-way function that hashes data.

---

**Attacks, Threats, and Vulnerabilities:**
---

Which of the following is true about false negatives in relation to vulnerability scanning tools?
\
I chose Is identified, and Is a high risk, but the answer is Is a high risk, and is not identified.
\
False negatives are the potential vulnerabilities that are not identified by the scanning tool. it is possible the vulnerability has not been discovered, or a hacker may have spoofed the vulnerability as if nothing is wrong.
\
A false negative is a high security risk because a possible threat could go unnoticed for long periods. This can be mitigated by running repeat scans and by using scanning tools from other vendors.
\
A false positive is something that is identified by a scanner or other assessment tool as being a vulnerability, when in fact it is not.
\
A false positive is not a high risk and more of a nuisance. Researching these issues cost time and effort.

---

A malicious actor successfully registered a domain called support247.onmicrosoft.com. This domain will be used to send emails to users to convince them to click the included to convince them to click the included links and attached files. Which social engineering technique is the malicious actor specifically using in this case?
\
I answered prepending but the answer is Typosquatting.
\
Typosquatting means that the threat actor registers a domain name that is very similar to a real one, such as connptia.org, hoping that users will not noticed the difference.
\
Reconnaissance is the overall preliminary surveying or research of an environment by any means. This may include social engineering, networking scans, or brute force.
\
Prepending means adding text that appears to have been generated by the mail system. For example, an attacker may add "RE:" to the subject line to make it appear legit.
\
Hybrid warfare is a hostile campaign that involves a suite of techniques to influence a target usually with a pollical agenda. It deploys espionage, disinformation/fake news, and hacking all in one.

---

Companies often update their website links to redirect users to new web pages that may feature a new promotion or to transition to a new web experience. How would an attacker take advantage of these common operations to lead users to fake versions of the website?
\
I answered Craft phishing links in email, and Hijack the website's domain, but the answers were Add redirects to .htaccess files, and Craft phishing links in email.
\
An attacker can craft a phishing link that might appear legitimate to a naive user, such as: https://trusted.foo/login.pgp?url="https://tru5ted.foo"
\
The .htacces file controls high-level configuration of a website. This file runs on an Apache server and can be edited to redirect users to other URLs.
\
A domain hijacking attack involves an adversary gaining control over the registration of a domain name, allowing the host records to be configured to IP addresses of the attacker's choosing.
\
Deliberately ruining company's reputation via online reviews and social media platforms can reduce user visitation to the website, which is less effective at luring users to a fake website.

---

Security admins are evaluating Windows server vulnerabilities related to Dynamic Link Library (DLL) injections. Modern applications are running on these Windows servers. How would an attacker exploit these vulnerabilities?
\
I answered Use malware with administrator privilege, Evade detection through refactoring, Navigate laterally using pass the hash, Enable legacy mode through shimming, but the correct answers were, Use malware with administrator privilege, Evade detection through refactoring.
\
The malware must evade detection by anti-virus to be successful. This can be done through code refactoring which means the code performs the same function by using different methods, such as changing its signature.
\
Dynamic Link Library (DLL) injection is deployed with malware that is already operating on the system with local administrator or system privileges.
\
Shimming is using code that intercepts and redirects calls to enable legacy mode exploiting the Windows Application Compatibility framework for DLL injections. The servers in this case used modern applications.
\
Pass the hash is a credential exploit technique. It harvests an account's cached credentials in a Single Sign-On (SSO) system and reuses the hash to authenticate to network protocols such as Server Message Block (SMB).

---

Which penetration technique allows a tester to bypass a network boundary and compromise servers on an internal network?
\
I answered Lateral movement, but the answer is Pivot.
\
A pivot bypasses a network boundary and compromises servers on an internal network. A pivot is normally accomplished using remote access and tunneling protocols.
\
A cleanup means removing evidence of the attack or evidence that could implicate the threat actor. An example would be removing any backdoors or other tools.
\
Lateral movement involved gaining control over other hosts. This can be done by harvesting credentials or detecting software vulnerabilities to widen access on the network.
\
Persistence is the tester's ability to reconnect to the compromised host and use it as a remote access tool (RAT) or backdoor. The tester must establish a command and control (C2 or C&C) network to use to control the compromised host.

---

An administrator goes through regular tasks every morning at the office to quickly gather health metrics of the network and associated systems. The admin connects to a Windows jump server using a secure shell (SSH) to run health scripts which outputs the data to a .xls file on a local shared folder accessible to all employees. The most recent run of the health script failed immediately without any indication of the issue. If an Information System Security Officer (ISSO) examined these morning tasks, what would be considered a weak configuration?
\
I answered Unsecure remote access, open permissions, and Unformatted error messages, but the answers were, Default settings and Open permissions.
\
Open permissions can allow anyone on the network with access to files and services. Although the file share is available to internal employees, only administrators should be reviewing gathered health information.
\
Default settings are usually unsecure settings that leave the environment and data open to compromise. A shared folder that provides access to everyone on the internal network is an example of a default setting when shared folder are created.
\
An unsecure protocol is one that transfers data as cleartext. Secure shell (SSH) provides encrypted data communication.
\
Weakly configured applications can sometimes display unformatted error messages. These messages can reveal vulnerabilities that a threat actor could take advantage of. No errors were revealed in this case.

---

Which of the following wireless technologies does not provide encryption and is known as a "bump"?
\
I answered RFID, but the answer is NFC.
\
Near Field Communication (NFC) is known as a bump, named after an early mobile sharing app. It was later redeveloped as android beam. It is commonly used for mobile wallet apps like google pay.
\
Radio frequency identification (RFID) is commonly used for asset management as tags. It is a chip programmed with asset data.
\
Initialization Vector (IV) is used in stream ciphers like in wireless network communication. The IV ensures the key produces a unique cyphertext from the same plaintext.
\
Bluetooth is a wireless radio technology that creates a personal area network (PAN). It is often used to connect to wireless speakers or vehicles for hands-free telecommunication.

---


Operations and Incident Response:
---

A junior engineer joins senior level staff in implementing cloud services using infrastructure as code. The junior engineer experiences confusion with playbooks and runbooks. Which options clarify the confusion?
\
I answered A playbook automates steps of a runbook, and A runbook is a checklist of actions, but the answers were a playbook is a checklist of actions, and a runbook automates steps of a playbook.
\
A runbook aims to automate as many stages of a playbook as possible, leaving clearly defined interactions points for human analysis.
\
An incident response workflow is usually defined as a playbook. A playbook is a checklist of actions to perform to detect and respond to a specific type of incident.
\
Where a playbook is implemented with a high degree of automation from a SOAR system, it can be referred to as a runbook.
\
SOAR assists the provision of runbooks, which orchestrate the sequence of response and automate parts of it. This is based off a checklist in a playbook.

---

Select the tools with which an attacker can identify misconfigured DNS servers with which a zone transfer can be performed, compromising the records of all hosts in a domain.
\
I answered nslookup/dig but the answer was dig, and nslookup/dig.
\
Querying name records for a given domain using a particular DNS resolver under Windows can be done with nslookup.
\
An attacker may test a network using dig on Linux systems to find out if the DNS service is misconfigured.
\
Curl is a command-line tool to transfer data to or from a server using supported protocols, such as HTTP, FTP, or IMAP.
\
tcpdump is a command-line packet capture utility for Linux. The utility will display captured packets until halted manually, and it can save frames to a .pcap file. This tool commonly uses filter expressions to reduce the number of frames captured, such as Type, Direction, or Protocol.

---

Identify which tools would be used to identify suspicious network activity.
\
I answered Wireshark, and tcpdump, but the answer was Wireshark, tcpdump and tcpreplay.
\
tcpdump is a command-line packet capture utility for Linux. The utility will display captured packets until halted manually, and it can save frames to a .pcap file. This tool commonly uses filter expressions to reduce the number of frames captured, such as Type, Direction, or Protocol.
\
Wireshark is a graphical application that can capture all types of traffic by sniffing the network, and save that data to a .pcap file.
\
tcpreplay is a command-line utility for Linux that can replay data from a .pcap file, for example, to analyze traffic patterns and data.
\
Metasploit is an exploitation framework that can identify vulnerabilities through penetration testing, but it is not useful for gathering real-time information that would identify attacks in progress.

---

Flow analysis tools, such as IPFIX or Netflow, collect metadata about network traffic without capturing each frame. Evaluate the type of analysis that uses these tools.
\
I answered Packet analysis, but the answer is trend analysis.
\
Since flow analyzers gather metadata and statistics about network traffic, they are commonly used to visualize traffic statistics in order to assist in identifying trends.
\
Packet analysis commonly performs through the use of protocol analyzers, like Wireshark. Also called packet sniffers, these tools capture individual packets, whereas flow analyzers do not.
\
Vulnerability scanners, such as Nessus, test for compliance with security standards and are commonly used to identify vulnerabilities in a system that needs to be patched.
\
Log analysis, often performed using a security information and event management (SIEM) dashboard, tracks the correlation between alert-able events and log entries.

---

Auditing SIP (Session Initiation Protocol)-based VoIP logs can reveal evidence of Man-in-the-Middle attacks. When handling requests, what do the call manager and any intermediate servers add to the SIP log file?
\
I answered A list of IP addresses of previous hops, but the answer is Their own IP address.
\
When managing requests, the call manager and all other intermediate servers add their IP address via the log header. The logs will show details of any Man-in-the-Middle attacks in which an unauthorized proxy intercepts data.
\
There is no need to add the IP address of the intended recipient to the log header.
\
The log header can easily determine the number of hops. However, hops are not explicitly counted as an integer, but obtained by counting the number of intermediate servers.
\
A list is not added to the log at each hop. Instead, a list is built by each intermediate server adding their own IP address to the header.

---

What are the main features that differentiate the Test Access Point (TAP) from a Switched Port Analyzer (SPAN)?
\
I answered Test access point (TAP) is a separate hardware device, Test access point (TAP) is considered 'active' only, Test access point (TAP) is a temporary solution, but the answers are Test access point (TAP) avoids frame loss, Test access point (TAP) is a separate hardware device.
\
A Test access point (TAP) is a hardware device that copies signals from the physical layer and the data link layer, while SPAN (switched port analyzer) is simply mirroring ports.
\
Since no network or transport logic is used with a test access point (TAP), every frame is received, allowing reliable packet monitoring.
\
Test access point (TAPs) can be either active or passive. Also, switched port analyzers (SPAN) are considered active.
\
Test access points (TAPs) are more stable and reliable than switched port analyzers (SPAN) and considered an investment as a long term solution; whereas, SPAN is more useful for temporary solutions.

---