Asterisk here means I got it right but was unsure:
- Docker uses namespaces to keep each container isolated to prevent one container from reading or writing processes in another.
- Control groups ensure that one container cannot overwhelm others in a DOS-type attack.
- Name spaces & control groups reduce the risk of data exposure between containers.
- The result of qualitative & Quanititative analysis is a measure of inherent risk.
- Control risk is a measure of how much less effective a security control has become over time.
- Inherent risk is the result of a qualititaties or quantitative risk analysis.
- Dual PDUs & a managed PDU ARE NOT a backup or failover, in a black out you'll go down. Generators > UPS however that comes at a cost.
- Data steward is like a librarian they just label the data and store it.
- Data processors engaged by data controller to assist w/ technical collection, storage, or analysis tasks, like me at USB.
- Data custodian is like the guy cleaning the data center fans in HVAC, they take care of the data.
- ACLs are a preventative control type.
- Corrective controls act to get rid of the baddies, that already got in.
- A [[runbook]] automates steps of a [[playbook]], & a [[playbook]] is a checklist of actions. Think, you run a [[runbook]].
- A fraud credit card purchase or opening a credit card is identity theft.
- DNS by default is insecure which is why DNSSec was created.
- If you dont want someone on your network to go to to a known malicious website/domain then instead you can send them to a DNS sinkhole, which is a site w/ a different IP.
- Linux directory access octets read like binary:
	- ...421 > RWX & the 3 options are owner, group & others.
- If initial Locking mechanism doesnt work, you would use:
	- compensating control (switch to plan B)
	- Preventative control (act to eliminate or reduce chance of attack)
- Embedded system uses combo of hardware and software that contains a dedicated function. (Think of low latency in a drone or UAV)
- VLANs are broadcast domains
- Ipv6 does not have broadcasts but does have multicast.
- STP (Spanning Tree Protocol) is a great way to control loops to prevent downtime.
- Bridge = switch
- BPDU is the primary protocol used by STP.
- MAC filtering is considered security through obscurity, so its not that safe.
- Context based authentication would use things like location services, time of day, or making sure youre on a safe network before you are allowed to connect to a program. (Think about how I need to use a VPN to connect to my work phone)
- SE Android is too specific use to be something that would help with connecting to a VPN.
- UEM may include MAM.
- Software development lifecycle: Dev -> Test -> Stage -> Prod
- Network security will use message authentication & block source routed packets, this stops spoofed IP addresses from making it through firewall/routers.
- IPv6 doesnt give you any extra security.
- Change management process is during code development process.
- CTFs & Gamification are both involving advancement & rewards for completing challenges like BOTS by Splunk.
- When you fill out a job application and it asks for things like "Sex, Veteran status, or race" this is all sensitive info, where as something like SSN or DOB is considered private info.
- With risk management youll want to find out what needs to be protected, then you want to figure out which is the most important, like confidential info, then prioritize that. So to start you will: Identify, Classify, Prioritize.
- CNs is a certificate attribute that will describe the computer it belongs to, but CNs are outdated so we now use SANs (Subject Alternative Names)
- Password entropy is how upredictable the password is.
- Too many incorrect login attempts locks out the account.
- Rc4 w/ TKIP is dated and whats used in WPA1
- Personal Wi-Fi authentication can use either 128-bit or 192-bit.
- If youre checking your code w/ a cx that is baseline configuration.
- When setting up cloud access management DONT use wildcards that is too vague and insecure.
- SDN uses ABAC that identifies subjects and objects within a policy.
- ACL are a good example of RBAC, Because it is based on a set of Allow/Deny rules.
- Things like encryption, code obfuscation, and signing can prevent data from being exposed & modified.
- Compilers DO NOT EXECUTE CODE, but do use SEH (Structured Exception Handling).
- IoT devices use Lightweight cryptography.
- ARO is Annual rate of occurence & is a quantifiable risk assessment that takes into account ALE.
- RPO (Recovery Point Objective), is basically how far back loss is 'Okay' because of your backups.
- RTO is the max time it takes to recover a system.
- MSA (Measured Systems Analysis) relates to quality management processes. Look into Sigma Six.
- A BPA (Business Partnership Agreement) is something like how microsoft or cisco provide equipment to resellers.
- A privacy officer is the law specialist in charge of managing all the business PII.
- A CIRT involving a decision maker from the business is important to be able to cope with various kinds of accidents.
- "Native Fire-wall Cost" is something charged hourly so it has nothing to do with attacks being attempted.
- High Latency API responses means there may be an attack.
- Lower # of rules = Lower Sensitivity & = Lower False Positives
- Higher # of rules = Higher Sensitivity & = Lower False Negatives
- MAC is like being able to access classified HR files you need to be both a 'Classified' label & 'HR' label. (Subjects & Objects).
- PAM is like a janitor needing to check out a key to get into a secure room. That process will need to be okayed and will be logged or audited by security because there is only one key to get into that room, this stops things like impersonation.
- A step by step plan for recovery is response & recovery control.
- Operational security controls refers to an item that can be physically touched. Meant to protect people, places, things.
- Control diversity means using multiple control types like a combo of admininistrator, technical, and physical.
- Dumps (memory & DNS) will not help find suspicious network traffic.
- TCG-SSC (Opal) has to do with SED.
- TCG-SSC = Trusted Computing group security subsystem class.
- Vuln Scanning is nonintrusive*
- UAC (User Account Control) & Sudo restrictions are conditional access.*
- Type I hypervisors are bare metal, no OS needed.*
- DLP systems & EPPs (Endpoint protection platforms) protect against a USB being used to steal data via copying.*
- Using Agile solution to constantly check code, thats continuous validation.*
- PAM is like the key analogy from Chris.*
- MAC is security clearance levels, w/ labels.*
- ARO x SLE = ALE*
- AI is a good way to use cloud resources to automate prediction & analysis to prevent future attacks.*
- Geographical dispersal is when the failover site must be seperate physcially from the program office & be available w/ live data on demand.*
- Failover clusters are like multiple servers used for load balancing, to maintain HA.*
- Artifacts are registry keys, files, timestamps, event logs, & these all may or may not be relevant for the investigation.*
- Data Sovereignty is when another jurisdiction wont give you the data.*
- Using security guards to protect construction is preventative & Operational.*
- Using a R-Pi or arduino to do a highly sensitive task is using a SoC.*
- A TAP (test access point) is hardware & can be permanent, provides no frame loss.*
- SPAN(Switched Port Analizers) are more temp & basically just mirrors ports.*
- SPAN is Active, & TAP is Passive or Active (on data link & physical layer)
- Best configuration management strategy to use to explain complex IT infrastructure to a new worker would be to use diagrams.*
- A Unified Threat Manager (UTM) is able to block URLs, Block malware, & Scan web traffic, but NOT encrypt traffic for that you would use a VPN.*
- MS-CHAPv2 can use PEAP for authentication*
- Change control is like an admin having to okay any change to directory access or clearance level changes.*
- Changing a network config from a file is considered SDN (Software Defined Networking).*
- Using a jumbox through a SSH server is a secure practice.*
- To protect your ML process you can just keep your ML algo a secret, and/or use a SOAR to check data properties.*
- Cloud access being comp'd is a way a threat actor is able to compromise a whole platform. (Not a supply chain attack though, thats different)*
- Managerial Security Control is one that oversees & monitors other controls for effectiveness*

---

Asterisk here means I knew I got it wrong:
- In a pentest proper rules of engagements would be things like: "steal files from server A" & "do not access production network", but something like "perform recon activities first" is a suggestion.*
- 802.11x or WPA3 uses EAP as its authentication mechanism.*
- AES is symmetrics 128, 192, or 256-bit block cypher. WPA2 uses AES.
- In configuring a DMZ w/ minimum configuration & security to rapidly deploy 2 web servers that are load balanced, the DMZ most likely has:*
	- Bastion Hosts (any server w/ min. services running in a DMZ)
	- Virtual IP Address (this is because of the load balancers)
	- Scheduling algorithm (think about round robin node processing)
- Security guidance offers a best practice summary analyzing the unique challanges of cloud environments & how on-prem controls can be adapted to them.* 
- Reference architecture offers a best practice methodology & tools for CSPs to use in architecting cloud solutions.
- To best acquire OS-level information from windows, you can:*
	- Check system & Security Logs
	- Reboot & Analyze memory dump files
	- Initiate sleep mode & analyze the hibernation file, @ the root of the boot volume.
- An application design flaw is not an example of a weak or improper application patch management, but these are:
	- Performance degradation
	- Unmanaged assets
	- No documentation
- Application design flaw is an example of a vulnerability.
- HTTPS in use: An encrypted TCP connection protects sensitive info during online transmission to a bank website.
- To acquire a disk image from a system you can:
	- Create snapshots of all volumes
	- save the disk image w/ a FTK imager
	- copy disk w/ dd command
- Hackers use phishing & adding redirects in the .htaccess files to take advantage of common business practices.
- Static code analysis is peer code review to identify oversights.*
- Dead code is executed but has no effect on the programs flow & should be removed.
- Runbooks & IRPs are guides for priorities & remediation.*
- To complete the solution of adding a NIDs you will need sensors.*
- Correlation engines are a part of a SIEM.
- A Gateway in an edge computing envrionment performs some preprocessing of data to enable prioritization, think about fog nodes.*
- A shared folder offering open access is default and thats insecure.*
- To create seperation across hardware & software devices just create VLANs.*
- In blackbox pen testing the first step should be to footprint.*
- Rules of engagement are set during hiring process of pentest consultant.*
- If using FTPS to transfer PII its best to use SSL/TLS, because this uses a CA to ensure the data is encrypted for confidentiality.
- IPSec is used to encrypt IP traffic. It encapsulates & encrypts data payloads.
- TCP is a network layer protocol that uses 3-way handshake.
- TACACS+ > RADIUS because it is easier to detect when a server is down, and it provides greater flexibility & reliability.*
- TACACS+ is more often used for device mgmt. than for authenticating end user devices. It allows centralized control of accounts set up to manage routers, switches, and firewall appliances.
- To avoid the client contacting the OCSP responder directly and exposing the identity of the certification requestor, use OCSP Stapling.*
- OCSP Stapling has the SSL/TLS server periodically get time stamped response from the CA. Then when the client submits an OCSP request the web server returns the timestamped response.
- LTE-m allows IoT devices to connect to 4G directly using baseband radio tech.*
- Zigbee is 2-way comms between Control system & sensors.
- Narrowband uses low powered LTE.
- FPGAs are an example of an embedded processor.
- If a company runs a local domain controller for directory services then plaintext API keys would be a vulnerability but NOT considered an attack.
- WPA3 & SAE are the most secure & up to date Wi-Fi configurations NOT EAP-TTLS because it uses CHAP and does not have anything to do with WiFi protection.*
- When performing analysis of a breached system and looking at data timestamps if theres time offset note UTC & Daylight savings.*
- Stateless firewalls are great because they let you block TCP ports & also allow network protocols.*
- Hardware firewalls generally have greater performance than software firewalls.
- Stateful firewalls like WAFs allow for things like comparing HTTP headers & HTML code to patterns in a threat database.
- Dead code being executed from an exploit is likely due to code reuse and not paying enough attention to what is being pushed to production.*
- Methods of containment that are also isolation are:
	- Blackhole or RTBH
	- Sandboxing
	- Physically disconnecting/air gapping
- A sinkhole routing means sus traffic gets routed to another network to be analyzed, this is considered network segmentation.
- In SaaS plans, the provider is responsible for the availability of the software. So in an IaaS model the architect will not need to worry about this.*
- If a company is taking NO measures or Security risk controls, then this company approaches risk during operation w/ Risk Acceptance.*
- Risk transference means assigning risk to a 3rd party.
- The discontinuation of a defective product is Risk Avoidance.
- WPA2 requires a longer password than WPA.*
- WPA is more secure than WEP because of RC-4 w/ TKIP.*
- Nessus will show you the CVE dictionary & CVSS score.
- When 2 companies first meet & want to maintain confidentiality and use a contract for intent to work together they use MOU.
- Part of the onboarding requirements for two companies that would like to include a mutual understanding of Quality management process they would be using MSA (Measured Systems Analysis).
- To ensure an application is secure before the release you should implement:
	- Input validation
	- Error Handling
	- Proper authentication & authorization
- Application audits should occur after the apps first commission or when the app gets upgrades, and regular intervals thereafter.
- An admin identifying & removing the cause of a malware attack in terms of the IRP procedure this step would be eradication.
- In a failover plan where connections are maintained even if performance is a little worse, the plan is likely using an active/active cluster or load balancer.
- AICPA & other finance representatives follow SSAE SOC2 type II, thats because SOC2 reports are highly detailed & designed to be restricted. Type II means the effectiveness of sec arch. over a period of 6-12 months.
- ISO 27K are security standards. 27002 classifies sec controls, 27001 focuses on personal data & privacy. Others reference cloud security.
- ISO 21K is a cybersec framwork, ISO 31K (3100) is an overall framwork for enterprise risk management.
- Under SOC3 a less detailed report is made for compliance w/ SOC 2. SOC3 reports can be freely distributed.
- Playbooks should always have SPECIFIC elements like:*
	- Incident catagories & definitions
	- When to report compliance incidents
	- Query strings to identify incident types. (This is to improve response and resolution times)
- Passwords & Private keys are never to be stored in a playbook or any document that could be viewed by unauthorized personnel.
- Just because someone downloads an APK and installs it does not mean the phone has been rooted. All we care about is that the APK file that was installed could be malicious or outdated.*
- Metadata that is to be associated w/ CDR (Call Detail Records):
	- SMS text timestamps
	- Call durations
	- List of towers connected to
	- We DONT care about GPS data
- Cache memory is more volatile than RAM.
- CN & SAN are certificate attributes that describes the computer or machine it belongs to.
- Honeynets & Sinkholes are both segmentation containment methods.
- How SIP-Based VoIP logs can show MiTM attacks is that call managers & intermediate servers add their own IP addresses to the SIP log file.
- ISACs (Information Security & Analysis Centers) & TAXII are both tools for best practice but actual IoCs that show any kind of TTPs from an attack would be things left behind like hardware (like a hardware TAP connected to a switch or Malicious USB drive/Rubber ducky) or logs.
- A DDoS on a local network from a threat actor would likely use:
	- Botnets
	- RAT
	- Command & Control (C2)
- When developing a BCP & the goal of the plan is to provide a potentially uninterrupted workflow in the event of an incident, then you would be ensuring processing redundancy supports the workflow.
- SAE is used in WPA3, and replaces WPAs normal 4 way handshake w/ a protocol based on the Diffie-Hellman key agreement.
- Even though EAP-Tunneled TLS creates an encrypted tunnel that uses server side certs, it is NOT something used for WiFi Protection.
- NGFWs are a generalized name for things such as:
	- Application layer gateway
	- Stateful Multilayer Inspection
	- Deep Packet inspection
- Intranets are employee only networks and are ONLY available internally. Its a PRIVATE network.
- Extranets are like DMZs however they are used for vendors and partners to have access to company resources.
	- This is different from an Intranet because those that connect will need to use some form of Authentication factors.
- In Data Centers theres 2 forms of traffic:
	- East and west
		- Traffic between devices in a data center to eachother
		- Much faster response times because theyre in the same building
	- North and South
		- Ingress/Egress to an outside device
		- Different security posture than east/west traffic
- TLS is the new name for SSL
- Network segmentation flavours:
	- Physical, logical, virtual
		- ex. Devices, VLANs, Virtual Networks, Air gaps.
	- Compliance like PCI is mandated Segmentation.
- Port 3389 is used for RDP
- Pulse secure is an example of an SSL VPN
- When there is site-to-site VPNs they commonly use L2TP (Layer 2 Tunneling Protocol) to connect to eachother as if theyre both actually connection via layer 2 but theyre actually connected from layer 3.
	- This is commonly used with IPsec like:
		- L2TP for the tunnel, IPsec for encryption
		- L2TP over IPsec (L2TP/IPsec)
- Chain of trust can be provided by:
	- Trusted Platform modules (TPMs)
	- Hardware Security Modules (HSMs)
- Screened subnet (Previously called DMZ)
	- Layer of Security between you & the internet
	- Public access only to public resources
- Static application security testing (SAST) is a great way to automate the scanning of applications that could contain malicious or suspect code, however it is not foolproof because sometimes there will be code that is using encryption that is weak and SAST will just see that it is at least encrypted so 'it must be safe'.
- IPsec is security for layer 3
	- Authenticate & Encrypt every packet
	- Offers packet signing for anti-replay
	- Very common
	- Two core IPsec protocols
		- Authentication Headers (AHs) - Hashed w/ SHA-2
		- Encapsulation Security Payloads (ESPs) - AES for encryption
- Transport vs. Tunnel mode: (Both have integrity checksums at the end)
	- Original Packet
		- Ip header|Data
	- Transport
		- Ip header|IPsec headers|Data|IPsec Trailers
	- Tunnel
		- New IP header|IPsec header|Data|IPsec Trailers



---

OSI Model: (7)

---

[Host Layers]
1: Application Layer - Data
2: Presentation Layer - Data
3: Session Layer - Data
4: Transport Layer - Segments
[Media Layers]
5: Network Layer - Packets
6: Datalink Layer - Frames
7: Physical Layer - Bits

---

OSI Layers Uses:

Host Layers:
- 1: Application Layer - Network process to application.
- 2: Presentation Layer - Data representation & Encryption.
- 3: Session Layer - Interhost Communication.
- 4: Transport Layer - End-to-End connections and reliablity
Media Layers:
- 5: Network Layer - Path determination & IP (Logical Addressing)
- 6: Datalink Layer - MAC and LLC (Physical Addressing)
- 7: Physical Layer - Media, Signal & Binary transmission

---

6 Phases of NIST IRP:

1) Prepare
2) Identify
3) Contain
4) Eradicate
5) Recover
6) Lessons learned

