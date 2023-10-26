# Q1:
An attacker is planning a cyber attack against a major organization. To learn more about the organization and its employees, the attacker used websites such as Facebook, Twitter, and LinkedIn. The attacker also researched the organization using other publicly available data such as news articles, the organization's website, and press releases.

What is the BEST way to describe this type of information gathering?

What did I answer?:
**Active reconnaissance**

Correct answer: **OSINT**

Open-source intelligence gathering, referred to as OSINT,  is the process of gathering information through public sources such as social media websites, company websites, news articles, public records, press releases, and more.

OWASP is the Open Web Application Security Project and is a non-profit organization that exists to help improve application security. Active reconnaissance refers to information gathering that requires interaction with the actual systems in a network, such as testing to find if ports are open on a network. Vulnerability scanning uses tools to locate common vulnerabilities within a network or system.

---

# Study
Below are questions I had flagged in my practice exams but got correct, Write out why I would be unsure about what the answer is and the correct answer in my own words that makes sense to me.

---

You are performing a penetration test in which you have been given no information about the target network. You will need to conduct open-source intelligence (OSINT) gathering as a means to learn more about the company and begin the simulated attack.

Which of the following BEST describes the type of test that you are performing?

Correct answer: Black box

A black box penetration test is completed by someone who is not familiar with the systems at all. The pen tester is not given much information about the network and must try to determine what vulnerabilities exist through their own reconnaissance and enumeration.

In a white box testing scenario, the pen tester knows the systems' internal workings and is given information such as credentials and source code. In a grey box testing scenario, the tester has some internal knowledge of the systems but still conducts the test as if they were an outside attacker. Sandboxing is a technique in which a program, code, or application is run in a controlled and monitored environment to see how it behaves; it is not a penetration testing method.

---

When using a system information and event management (SIEM) solution, it is crucial to ensure that nobody is able to modify log entries.

What term is used to describe this functionality?

Correct answer: WORM

If individuals are able to modify log entries, the integrity of the logs is not intact. As such, it is crucial that the logs are not able to be modified once they enter the SIEM solution. WORM (write once, read many) is the idea that once a log entry is received, the SIEM will aggregate and correlate them. After processing the logs, it archives the source logs with write protection.

---

You are interested in implementing a solution that will act as a central repository for all logs and provide a means to aggregate and correlate those logs.

Which type of solution would BEST fit your needs?

Correct answer: SIEM

A security information and event management (SIEM) solution can be used as a central repository for monitoring and system logs. Additionally, these types of products provide a helpful way to aggregate and correlate events as well as provide alerting functionality. ArcSight, QRadar, and Splunk are examples of popular SIEM solutions.

---

While working in a security operations center (SOC), you are reviewing a piece of malicious code. The code works by attaching itself to a host application and, once executed, replicating itself throughout other applications. Throughout your investigation, you determine that the code isn't able to run on its own. It requires that its host application be executed for it to run.

What is the name for this type of malicious code?

Correct answer: Virus

A virus is a type of malicious code that can attach itself to a host application. For the virus to run, the host application must be executed. Once the virus is run, it replicates throughout a system, infecting other applications that become host applications for that virus.

Worms are similar to viruses; however, they are self-replicating and don't require user interaction or a host application. A bot is an infected system that is under the control of an attacker. A remote access trojan (RAT) is a trojan type that provides remote access to a system while bypassing typical authentication methods.

---

An attack has compromised an organization's systems. Upon gaining access, the attacker began transferring corporate confidential data outside of the network to systems under the attacker's control.

What is being described in this scenario?

Correct answer: Data exfiltration

Data exfiltration refers to the unauthorized transfer of confidential data outside of the organization. Data exfiltration can be accomplished through various attacker methods such as malware or even a malicious insider saving data on a USB drive and taking it out of the network. To prevent data exfiltration, data loss prevention (DLP) solutions should be implemented.

---

An organization recently faced a major data breach that cost them millions of dollars. Upon investigation, security analysts found that the breach resulted from a known vulnerability in the Windows operating system. Microsoft had released an update to resolve the issue, but it was not installed on the machine at the time of the breach.

Which of the following solutions could have BEST prevented this breach?

Correct answer: Patch management

Patch management refers to the planning, testing, and installation of patches/updates. Without patch management, it can be difficult to ensure that all systems are patched and protected from known vulnerabilities.

Data loss prevention (DLP) technologies help to prevent the exfiltration of data after an exploit, but it would have been the patch that would have prevented the breach. There is no indication that application blacklisting or removable media control would have prevented this breach.
