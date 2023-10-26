Sources:
https://resources.infosecinstitute.com/certification/the-security-cbk-domains-information-and-updates/
\
21% of the CompTIA SEC+ exam exam:
\
Now it is time to put this knowledge to good use and demonstrate that you can apply security controls in practice and create a safe environment for company operations. This domain will require candidates to explain use cases and purposes for frameworks, best practices and secure configuration guides. It is also necessary to understand how to create [[Benchmark]]s/[[Secure_Configuration_Guide]]s and how to use the concepts of [[Defense-in-Depth]] and layers as the basis for a secure architecture. Questions are especially focused on [[Cloud]] technology due to the growing reliance of organizations on hybrid networks.
\
It is quite obvious that creating a safe design is just the first step, so candidates must demonstrate the ability to implement secure network architecture concepts when creating a secure topology with different zones (e.g., [[DMZ]], [[Intranet]], [[Extranet]], wireless, [[Honeypot]]), each with specific controls.
\
Embedded systems must also be protected, so candidates need to understand the security implications related to Supervisory Control And Data Acquisition ([[SCADA]]) and Industrial Control Systems ([[ICS]]) in general. But it does not stop there; candidates need to consider the protection of [[Smart_Device]]s (e.g., wearables) and security controls for [[IoT]] (Internet of Things), proper protection of heating, ventilation, and air conditioning ([[HVAC]]) systems, camera systems ([[PTZ]] Cameras, [[CCTV]] cameras), and even special-purpose technology such as medical devices, smart vehicles, [[Drones]] and unmanned aerial vehicles ([[UAV]]s).
\
Other topics related to secure Architecture and Design include summarizing secure application development and deployment concepts such as [[Life-Cycle_Models]], secure [[DevOps]] ([[DevSecOps]]), secure coding techniques, and code quality and testing, understanding cloud and [[Virtualization]] concepts including the use of different types of [[Hypervisor]]s, cloud storage, cloud deployment models ([[SaaS]], [[PaaS]], [[IaaS]], [[Private_Cloud]], [[Public_Cloud]], [[Hybrid_Cloud]] and [[Community_Cloud]]) the differences and security advantages of multiple strategies ([[On-Premise]] vs. hosted vs. [[Cloud]]) and the concepts of cloud access security broker ([[CASB]]) and security as a service ([[SECaaS]]).
\
Candidates are also required to know the importance of physical security controls such as physical barriers ([[Bollards]], fencing, gate and cage), having security guards, proper signs, alarms, locks and cameras, the use of motion detection and key management.
# 2.0 Architecture and Design

## 2.1 Explain the importance of security concepts in an enterprise environment.

---
- [ ] • Configuration management
	-Diagrams
	-Baseline configuration ([[Baseline_Security]])
	-Standard naming conventions ([[CN]])
	-Internet protocol ([[IP]]) [[Schema]]s
- [ ] • [[Data_Sovereignty]]
- [ ] • Data protection
	-Data loss prevention ([[DLP]])
	-[[Masking]]
	-[[Encryption]]
	-[[Data_at_Rest]]
	-[[Data_in_Transit]] [[Data_in_Motion]]
	-[[Data_in_Processing]]
	-Tokenization [[Token]] [[Token-Based_Authentication]]
	-[[Rights_Management]]
- [ ] • Geographical considerations
- [ ] • Response and recovery controls
- [ ] • Secure Sockets Layer ([[SSL]])/Transport Layer Security ([[TLS]]) inspection
- [ ] • [[Hashing]]
- [ ] • [[API]] considerations
- [ ] • Site resiliency
	-[[Hot_Site]]
	-[[Cold_Site]]
	-[[Warm_Site]]
- [ ] • Deception and disruption
	-[[Honeypot]]s
	-[[Honeyfile]]s
	-[[Honeynet]]s
	-[[Fake_Telemetry]] / [[Telemetry]]
	-[[DNS_Sinkhole]]

## 2.2 Summarize virtualization and cloud computing concepts.

---
- [ ] • Cloud models
	-Infrastructure as a service ([[IaaS]])
	-Platform as a service ([[PaaS]])
	-Software as a service ([[SaaS]])
	-Anything as a service ([[XaaS]])
	-[[Public_Cloud]]
	-[[Community_Cloud]]
	-[[Private_Cloud]]
	-[[Hybrid_Cloud]]
- [ ] • Cloud service providers ([[CSP]]s)
- [ ] • Managed service provider ([[MSP]])/ managed security service provider ([[MSSP]])
- [ ] • [[On-premise]]s vs. Off-Premises
- [ ] • [[Fog_Computing]]
- [ ] • [[Edge_Computing]]
- [ ] • [[Thin_Client]]
- [ ] • [[Container]]s
- [ ] • Microservices/[[API]]
- [ ] • Infrastructure as code
	-Software-defined networking ([[SDN]])
	-Software-defined visibility ([[SDV]])
- [ ] • [[Serverless_Architecture]]
- [ ] • Services integration
- [ ] • Resource policies
- [ ] • Transit gateway
- [ ] • Virtualization
	-Virtual machine ([[VM]]) [[Sprawl_Avoidance]]
	-[[VM_Escape]] protection

## 2.3 Summarize secure application development, deployment, and automation concepts.

---
- [ ] • Environment
	-[[Development_Environment]]
	-[[Test_Environment]]
	-[[Staging]]
	-[[Production_Environment]]
	-[[Quality_Assurance]] ([[QA]])
- [ ] • [[Provisioning]] and deprovisioning
- [ ] • [[Integrity]] measurement
- [ ] • Secure coding techniques
	-[[Code_Normalization]]
	-[[Stored_Procedures]]
	-[[Obfuscation]]/[[Camouflage]]
	-[[Code_Reuse]]/[[Dead_Code]]
	-[[Server-side_Code_Validation_and_Execution]] vs. [[Client-side_Code_Validation_and_Execution]]
	-Memory management
	-Use of third-party libraries and software development kits ([[SDK]]s)
	-[[Data_Exposure]]
- [ ] • Open Web Application Security Project ([[OWASP]])
- [ ] • Software diversity
	-[[Compiler]]
	-[[Binary]]
- [ ] • [[Automation]]/[[Script]]ing
	-[[Automated_Courses_of_Action]] ([[ACOA]])
	-[[Continuous_Monitoring]]
	-[[Continuous_Validation]]
	-[[Continuous_Integration]]
	-[[Continuous_Delivery]]
	-[[Continuous_Deployment]]
- [ ] • [[Elasticity]]
- [ ] • [[Scalability]]
- [ ] • [[Version_Control]]

## 2.4 Summarize authentication and authorization design concepts.

---
- [ ] • Authentication methods
	-[[Directory_Services]]
	-[[Federation]]
	-[[Attestation]]
	-Technologies
	-Time-based one-time password ([[TOTP]])
	-[[HMAC]]-based one-time password ([[HOTP]])
	-Short message service ([[SMS]])
	-[[Token]] key
	-[[Static_Codes]]
	-Authentication applications
	-[[Push_Notification]]s
	-Phone call
	-[[Smart_Card]] authentication
- [ ] • [[Biometrics]]
	-Fingerprint
	-Retina
	-Iris
	-Facial
	-Voice
	-Vein
	-[[Gait_Analysis]]
	-Efficacy rates
	-[[False_Acceptance]]
	-[[False_Rejection]]
	-[[Crossover_Error_Rate]]
- [ ] • Multifactor authentication ([[MFA]]) factors and attributes
	-[[Authentication_Factors]]
	-Something you know
	-Something you have
	-Something you are
	-[[Authentication_Attributes]]
	-Somewhere you are
	-Something you can do
	-Something you exhibit
	-Someone you know
- [ ] • Authentication, authorization, and accounting ([[AAA]])
- [ ] • Cloud vs. on-premises requirements

## 2.5 Given a scenario, implement cybersecurity resilience.

---
- [ ] • Redundancy
	-Geographic dispersal
	-[[Disk_Redundancy]]
	-Redundant array of inexpensive disks ([[RAID]]) levels
	-Multipath
	-[[Network]]
	-[[Load_Balancer]]s
	-Network interface card ([[NIC]]) teaming
	-Power
	-Uninterruptible power supply ([[UPS]])
	-Generator
	-Dual supply
	-Managed power distribution units ([[PDU]]s)
- [ ] • Replication
	-[[Storage_Area_Network]] ([[SAN]])
	-[[VM]]
- [ ] • On-premises vs. cloud
- [ ] • Backup types
	-[[Full_Backup]]
	-[[Incremental_Backup]]
	-[[Snapshot]]
	-[[Differential_Backup]]
	-Tape
	-Disk
	-Copy
	-[[Network-attached_Storage]] ([[NAS]])
	-[[Storage_Area_Network]]
	-[[Cloud]]
	-[[Image_Backup]]
	-Online vs. offline
	-[[Offsite_Storage]]
	-Distance considerations
- [ ] • Non-persistence
	-Revert to known state
	-Last known-good configuration
	-[[Live_Boot_Media]]
- [ ] • [[High_Availability]]
	-[[Scalability]]
- [ ] • [[Restoration_Order]]
- [ ] • Diversity
	-[[Technology_Diversity]]
	-[[Vendors_Diversity]]
	-[[Crypto_Diversity]]
	-[[Control_Diversity]]

## 2.6 Explain the security implications of embedded and specialized systems.

---
- [ ] • [[Embedded_System]]s
	-[[Raspberry_Pi]]
	-Field-programmable gate array ([[FPGA]])
	-[[Arduino]]
- [ ] • Supervisory control and data acquisition ([[SCADA]])/industrial control system ([[ICS]])
	-Facilities
	-Industrial
	-Manufacturing
	-Energy
	-Logistics
- [ ] • Internet of Things ([[IoT]])
	-Sensors
	-[[Smart_Device]]s
	-Wearables
	-[[Facility_Automation]]
	-[[Weak_Default]]s
- [ ] • Specialized
	-Medical systems
	-Vehicles
	-Aircraft
	-[[Smart_Meter]]s
- [ ] • Voice over IP ([[VoIP]])
- [ ] • Heating, ventilation, air conditioning ([[HVAC]])
- [ ] • [[Drones]]
- [ ] • Multifunction printer ([[MFP]])
- [ ] • Real-time operating system ([[RTOS]])
- [ ] • Surveillance systems
- [ ] • System on chip ([[SoC]])
- [ ] • Communication considerations
	-5G
	-[[Narrow-Band]]
	-[[Baseband_Radio]]
	-Subscriber identity module ([[SIM]]) cards
	-[[Zigbee]]
- [ ] • Constraints
	-Power
	-Compute
	-Network
	-Crypto
	-Inability to patch
	-Authentication
	-Range
	-Cost
	-Implied trust

## 2.7 Explain the importance of physical security controls.

---
- [ ] • [[Bollards]]/[[Barricades]]
- [ ] • [[Access_Control_Vestibules]]
- [ ] • [[Badge]]s
- [ ] • Alarms
- [ ] • [[Signage]]
- [ ] • Cameras
	-Motion recognition
	-[[Object_Detection]]
- [ ] • Closed-circuit television ([[CCTV]])
- [ ] • [[Industrial_Camouflage]]
- [ ] • Personnel
	-Guards
	-[[Robot_Sentries]]
	-Reception
	-[[Two-person_Integrity]]/control
- [ ] • Locks
	-[[Biometrics]]
	-Electronic
	-Physical
	-[[Cable_Locks]]
- [ ] • [[USB_Data_Blocker]]
- [ ] • Lighting
- [ ] • Fencing
- [ ] • [[Fire_Suppression]]
- [ ] • Sensors
	-[[Motion_Detection]]
	-[[Noise_Retection]]
	-[[Proximity_Reader]]
	-[[Moisture_Detection]]
	-[[Card_Sensors]]
	-[[Temperature_Sensors]]
- [ ] • [[Drones]]
- [ ] • [[Visitor_Logs]]
- [ ] • [[Faraday_Cages]]
- [ ] • [[Air_Gap]]
- [ ] • [[Screened_Subnet]] (previously known as [[Demilitarized_Zone]]/[[DMZ]])
- [ ] • Protected cable distribution
- [ ] • Secure areas
	-[[Air_Gap]]
	-Vault
	-Safe
	-[[Hot_Aisle]]
	-[[Cold_Aisle]]
- [ ] • [[Secure_Data_Destruction]]
	-Burning
	-Shredding
	-Pulping
	-Pulverizing
	-[[Degauss]]
	-Third-party solutions

## 2.8 Summarize the basics of cryptographic concepts

---
- [ ] • [[Digital_Signatures]]
- [ ] • [[Key_Length]]
- [ ] • [[Key_Stretching]]
- [ ] • [[Salt]]ing
- [ ] • [[Hashing]]
- [ ] • [[Key_Exchange]]
- [ ] • [[Elliptic-curve_Cryptography]]
- [ ] • [[Perfect_Forward_Secrecy]]
- [ ] • Quantum
	-[[Quantum_Communication]]s
	-[[Quantum_Computing]]
- [ ] • [[Post-Quantum]]
- [ ] • [[Ephemeral]]
- [ ] • Modes of operation
	-[[Authenticated_Encryption]]
	-[[Unauthenticated_Encryption]]
	-Counter ([[GCM]])
- [ ] • [[Blockchain]]
	-[[Public_Ledger]]s
- [ ] • Cipher suites
	-[[Stream_Cypher]]
	-[[Block_Cypher]]
- [ ] • [[Symmetric_Encryption]] vs. [[Asymmetric_Encryption]]
- [ ] • [[Lightweight_Cryptography]]
- [ ] • [[Steganography]]
	-Audio
	-Video
	-Image
- [ ] • [[Homomorphic_Encryption]]
- [ ] • [[Common_Encryption_Use_Cases]]
	-Low power devices
	-[[Low_Latency_Cryptography]]
	-[[High_Resiliency]]
	-Supporting [[Confidentiality]]
	-Supporting [[Integrity]]
	-Supporting [[Obfuscation]]
	-Supporting [[Authentication]]
	-Supporting [[Non-Repudiation]]
- [ ] • [[Encryption_Limitations]]
	-Speed
	-Size
	-Weak keys
	-Time
	-Longevity
	-Predictability
	-Reuse
	-[[Entropy]]
	-[[Computational_Overhead]]s
	-Resource vs. security constraints


# Acronyms used in this domain of the exam:

---
[[ACOA]]
[[AAA]]
[[API]]

[[CASB]]
[[CN]]
[[CCTV]]
[[CSP]]

[[DLP]]
[[DMZ]]
[[DNS]]

[[HMAC]]
[[HOTP]]
[[HVAC]]

[[ICS]]
[[IOT]]
[[IP]]
[[IAAS]]
[[ICS]]

[[MSP]]
[[MSSP]]
[[MFA]]
[[MFP]]

[[NAS]]
[[NIC]]

[[OWASP]]

[[PAAS]]
[[PTZ]]
[[PDU]]

[[QA]]

[[RTOS]]
[[RAID]]

[[SECaaS]]
[[SDN]]
[[SDV]]
[[SAAS]]
[[SSL]]
[[SCADA]]
[[SAN]]
[[SoC]]
[[SIM]]
[[SMS]]
[[SDK]]

[[TOTP]]
[[TLS]]

[[UAV]]
[[UPS]]

[[VPC]]
[[VoIP]]
[[VM]]

[[XaaS]]
