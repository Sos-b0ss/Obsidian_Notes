Sources:
https://www.fortinet.com/resources/cyberglossary/what-is-soar
https://www.paloaltonetworks.com/cyberpedia/what-is-soar
https://www.crowdstrike.com/cybersecurity-101/security-orchestration-automation-and-response-soar/
\
Some common [[SOAR]] products frequently used within the industry:  
-   [[Splunk]] Phantom
-   IBM Resilient
-   Logsign
-   Demisto
\
 It enables the security products and tools within an environment to work together and therefore makes the [[SOC]] team members' jobs easier. For example it will automatically perform a search for the source [[IP]] of a [[SIEM]] alert in Virustotal and so it lightens the load of the [[SOC]] analyst.
\
![[Pasted image 20220709115246.png]]
\
Benefits of using a [[SOAR]] are:

**Saves Time**
[[SOAR]] saves time through workflows that automate processes. Some frequently used workflows are:
-   [[IP]] address repetition control
-   [[Hash]] query
-   Scanning an acquired file in a [[Sandbox]] environment


**Centralization**
It enables the operation of various security tools in your environment ([[Sandbox]], log managements, 3rd party tools, etc) from one point. These tools are integrated into the [[SOAR]] solution and can be used on the same platform.
\
![[Pasted image 20220709115458.png]]
\
**Playbook**

We can easily investigate [[SIEM]] alerts using playbooks created for various scenarios within [[SOAR]]. These playbooks help us conduct an analysis because we can follow the instructions even though we don’t know or remember all the steps of the analysis.
\
Additionally, these [[Playbook]] help the whole [[SOC]] team to conduct their analyses on the same plane. For example, if one team member is not checking [[IP]] reputation and the others are, then this is an undesirable situation, we want all team members to check [[IP]] reputation. We can prevent this situation by adding this step to the playbook.
