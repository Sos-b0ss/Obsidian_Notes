Data that we run through feeds that does not show up:
\
Let’s say we ran a hash that belonged to an .exe in VirusTotal and could not find anything suspicious about it in the past. We should not suppose that the file is clean, this would be a mistake. Still, we should be diligent about performing the required file analyses (static/dynamic).
\
We shouldn’t forget that IP addresses can change hands:

For example, let’s say an attacker created a server over AWS and used it as a command and control center. Then various threat intelligence feeds recorded this IP address on their lists as a malicious address.
\
Like any person, SOC analysts also make mistakes. In this section we will mention mistakes that are frequently made by SOC analysts and discuss how we can avoid making these mistakes ourselves.

-   Overly Depending on VirusTotal Results
-   Hasty Analysis of Malware in a Sandbox
-   Insufficient Log Analysis
-   Overlooking VirusTotal Dates