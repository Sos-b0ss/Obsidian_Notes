Sources:
https://resources.infosecinstitute.com/certification/the-security-cbk-domains-information-and-updates/
https://www.cisa.gov/free-cybersecurity-services-and-tools
\
16% of the CompTIA SEC+ exam exam:
\
This domain is about the role of the security professional in the response to an incident. It covers anything from incident handling to disaster recovery and business continuity. The exam addresses both technical and administrative concepts. It not only tests on forensics, network reconnaissance and discovery concepts and the ability to reconfigure systems for incident mitigation, but it also covers the preparation phase that allows a business to be ready for unfortunate events like attacks: from tabletop exercises and simulations to the creation of plans. ([[CP]], [[COOP]], [[ERP]], [[ITCP]], [[PoA]], and [[CNAP]])
\
Considering that some risks will eventually become real occurrences, candidates must understand the procedures for dealing with security incidents, such as creating a formal incident response plan ([[IRP]]) that defines the methods for incident documentation and classification, clear roles and responsibilities, escalation procedures and who is the cyber-incident response team ([[CSIRT]], [[CIRT]]). Of course, the incident response process must also be considered, including phases such as preparation, identification, containment, eradication, recovery and lessons learned. ([[IR]])
\
Candidates must understand and be able to explain concepts such as the different types of recovery sites (i.e., [[Hot_Site]], [[Warm_Site]] and [[Cold_Site]]), how to define the order of system/business processes restoration, how to use the different types of backup ([[Differential_Backup]], [[Incremental_Backup]], [[Snapshot]]s and [[Full_Backup]]), the geographic considerations when choosing a disaster recovery strategy ([[DRP]]), such as having [[Off-site_Backup]]s, what is the necessary distance between the production environment and recovery facilities, even legal implications (i.e. can data be stored/recovered in a different country?) and a key point: how the continuity of operations will be tested to confirm disaster recovery plans work. ([[BCP]])
\
Testers are also required to summarize basic concepts of forensics, including the order of [[Volatility]], creating and maintaining a [[Chain_of_Custody]] , legal hold, data acquisition and preservation, recovery techniques and strategic intelligence/counterintelligence gathering. Basically, the candidate needs to be able to demonstrate the knowledge necessary not only to gather data needed for the investigation, but also to preserve it both from a technical and a legal perspective.
# 4.0 Operations and Incident Response

---

## 4.1 Given a scenario, use the appropriate tool to assess organizational security.

---
- [ ] • Network [[Reconnaissance]] and discovery
	-[[Tracert]]/[[Traceroute]]
	-[[Nslookup]]/[[Dig]]
	-[[Ipconfig]]/[[Ifconfig]]
	-[[Nmap]]/[[Nikto]]
	-[[Ping]]/[[Pathping]]
	-[[Hping]]
	-[[Netstat]]
	-[[Netcat]]
	-[[IP]] scanners (ex. [[Curl]] ifconfig.co)
	-[[Arp]]
	-[[Route]]
	-[[Curl]]
	-[[TheHarvester]]/[[Nagios]]/[[Argus]]
	-[[Sn1per]]/[[Paros_Proxy]]
	-[[Scanless]]
	-[[Dnsenum]]
	-[[Nessus]]
	-[[Cuckoo]]
- [ ] • File manipulation
	-[[Head]]
	-[[Tail]]
	-[[Cat]]
	-[[Grep]]
	-[[Chmod]]
	-[[Logger]]
- [ ] • Shell and script environments
	-[[SSH]]
	-[[PowerShell]]
	-[[Python]]
	-[[OpenSSL]]
- [ ] • Packet capture and replay
	-[[Tcpreplay]]
	-[[Tcpdump]]
	-[[Wireshark]] ([[Snort]], [[Splunk]])
- [ ] • Forensics
	-[[Dd]]
	-[[Memdump]]
	-[[WinHex]]
	-[[FTK_Imager]]
	-[[Autopsy]]
- [ ] • Exploitation frameworks (ex. [[Metasploit]], [[Xerosploit]], [[Nexpose]], [[W3af]])
- [ ] • Password crackers (ex. [[John_The_Ripper]], [[HashCat]], [[CrackStation]], [[Aircrack]])
- [ ] • Data sanitization ([[OSSEC]])

## 4.2 Summarize the importance of policies, processes, and procedures for incident response.

---
- [ ] • Incident response plans ([[IRP]])
- [ ] • Incident response process
	-[[Preparation_Phase]]
	-[[Identification_Phase]]
	-[[Containment_Phase]]
	-[[Eradication_Phase]]
	-[[Recovery_Phase]]
	-Lessons learned
- [ ] • Exercises
	-Tabletop
	-Walkthroughs
	-Simulations
- [ ] • Attack frameworks
	-[[MITRE]] [[ATT&CK]]
	-[[The_Diamond_Model_of_Intrusion_Analysis]]
	-[[Cyber_Kill_Chain]]
- [ ] • Stakeholder management
- [ ] • Communication plan 
- [ ] • Disaster recovery plan ([[DRP]])
- [ ] • Business continuity plan ([[BCP]])
- [ ] • Continuity of operations planning ([[COOP]])
- [ ] • Incident response team ([[CIRT]])
- [ ] • Retention policies

## 4.3 Given an incident, utilize appropriate data sources to support an investigation.

---
- [ ] • Vulnerability scan output
- [ ] • [[SIEM]] dashboards
	-Sensor
	-Sensitivity
	-Trends
	-Alerts
	-Correlation
- [ ] • Log files
	-[[Network]]
	-System
	-Application
	-Security
	-Web
	-[[DNS]]
	-[[Authentication]]
	-Dump files ([[Tcpdump]])
	-[[VoIP]] and call managers
	-Session Initiation Protocol ([[SIP]]) traffic
- [ ] • [[Syslog]]/[[Rsyslog]]/[[Syslog-ng]]
- [ ] • [[Journalctl]]
- [ ] • [[NXLog]]
- [ ] • [[Bandwidth_Monitor]]s
- [ ] • [[Metadata]]
	-Email
	-Mobile
	-Web
	-File
- [ ] • [[Netflow]]/[[sFlow]]
	-[[Netflow]]
	-[[sFlow]]
	-[[IPFIX]]
- [ ] • [[Protocol_Analyzer]] output

## 4.4 Given an incident, apply mitigation techniques or controls to secure an environment.

---
- [ ] • Reconfigure [[Endpoint_Security_Solutions]] ([[ETDR]], [[EDR]])
	-[[Application_Approved_List]]
	-[[Application_Blocklist]]/deny list
	-[[Quarantine]]
- [ ] • Configuration changes
	-[[Firewall]] rules
	-[[MDM]]
	-[[DLP]]
	-[[Content_Filter]]/[[URL]] filter
	-Update or revoke [[Certificate]]s
- [ ] • [[Isolation]]
- [ ] • [[Containment]]
- [ ] • [[Segmentation]]
- [ ] • [[SOAR]]
	-[[Runbook]]
	-[[Playbook]]

## 4.5 Explain the key aspects of digital forensics.

---
- [ ] • Documentation/evidence
	-Legal hold
	-Video
	-Admissibility
	-[[Chain_of_Custody]]
	-Timelines of sequence of events
	-Time stamps
	-Time offset
	-[[Tags]]
	-Reports
	-[[Event_Logs]]
	-Interviews
- [ ] • Acquisition
	-[[Order_of_Volatility]]
	-Disk ([[SSD]], [[HDD]], [[NVME]])
	-Random-access memory ([[RAM]])
	-[[Swap]]/[[Pagefile]]
	-[[OS]]
	-Device ([[MAC]])
	-[[Firmware]]
	-[[Snapshot]]
	-[[Cache]]
	-Network
	-[[Artifacts]]
- [ ] • [[On-premise]]s vs. [[Cloud]]
	-[[Right-to-audit_Clause]]s
	-Regulatory/[[Jurisdiction]]
	-Data breach notification laws ([[HIPAA]], [[GLBA]], [[FDIC]])
- [ ] • [[Integrity]]
	-[[Hashing]] ([[MD5]], [[SHA]], [[SHA-256]])
	-[[Checksum]]s
	-[[Data_Provenance]]
- [ ] • Preservation
- [ ] • [[E-Discovery]]
- [ ] • Data recovery
- [ ] • [[Non-Repudiation]]
- [ ] • Strategic intelligence/[[Counterintelligence]]

# Acronyms used in this domain of the exam:

---

[[ATT&CK]]

[[BCP]]

[[CIRT]]
[[CNAP]]
[[COOP]]
[[CP]]
[[CSIRT]]

[[DLP]]
[[DNS]]
[[DRP]]

[[EDR]]
[[ERP]]
[[ETDR]]

[[FDIC]]

[[GLBA]]

[[HDD]]
[[HIPAA]]

[[IDS]]
[[IPS]]
[[IR]]
[[IRP]]
[[ITCP]]

[[MAC]]
[[MD5]]
[[MDM]]

[[NIDS]]
[[NIPS]]
[[NVME]]

[[OS]]

[[PoA]]

[[RAM]]

[[SHA]]
[[SHA-256]]
[[SIEM]]
[[SIP]]
[[SOAR]]
[[SSD]]
[[SSH]]
[[SSL]]

[[URL]]

[[VoIP]]
