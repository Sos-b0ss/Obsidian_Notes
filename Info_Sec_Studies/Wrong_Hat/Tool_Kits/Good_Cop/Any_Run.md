Sources:
https://any.run/
\
[AnyRun](https://any.run/) is an interactive sandbox that you can use when you want to analyze malware quickly.
\
AnyRun has options for paid or free use. If you want to take advantage of it for free, all your analysis is visible to others, therefore we do not recommend that you upload files that may contain personal data to AnyRun. In addition, the free plan has restrictions such as usage time.
\
Basically a clone of just using something like [[Kasm]] with [[RemNUX]]
\
Here's a tutorial from LetsDefend:
---
How can we use AnyRun for our malware analysis, what kind of outputs we can get, let's examine it together.

Let's download the malware with hash **80b51e872031a2befeb9a0a13e6fc480** to analyze via [AbuseCH](https://bazaar.abuse.ch/sample/708e198608b5b463224c3fb77fcf708b845d0c7b5dbc6e9cab9e185c489be089/).

We have to click on the "**+**" **(New Task)** button on the left menu to upload the malware we downloaded.

![](https://letsdefend.io/blog/wp-content/uploads/2021/01/Screen-Shot-2021-01-26-at-22.48.58.png)

Let's upload the file we want to analyze on the screen that opens with the help of the "Choose a file" button. After the file is uploaded, we can determine the parameters such as which operating system we want to run the malware and 32/64 bit of operating system to use. After determining these, we open our sandbox with the help of the "**Run**" button at the bottom right of the screen that opens.

When our machine is turned on, we run the malicious software we uploaded to see it's activities.

Some malware stays dormant for a certain period of time before performing its malicious activities, making analysis difficult. Let's allow time for the malware to perform its activities, during this time, let's examine the AnyRun interface together.

![](https://letsdefend.io/blog/wp-content/uploads/2021/01/Screen-Shot-2021-01-26-at-22.58.53-scaled.jpg)

1.  From this area, you can use the operating system interactively.
2.  Here is a list of processes in this section. From here, you can easily see which childprocesses the malware you run has.
3.  In this area there is network and files events.
4.  This section contains details of the process.

Let's examine these outputs.

First, let's examine the process events of the malware in the section marked "2" in the image above.

![](https://letsdefend.io/blog/wp-content/uploads/2021/01/Screen-Shot-2021-01-26-at-23.11.38.png)

The malware we run manually seems to have created 2 child processes. One of them is **schtasks.exe**, which is run to ensure persistence on the system by creating a schedule task and the other is the process specified as "**AgentTesla**" malware by AnyRun.

When we click on Processes, information about this process is displayed in panel number 4. Let's examine the details of all processes respectively.

Since the process named "WinRAR.exe" is created when we extract the malware from the archive file to run it, we will not examine this process.

When we click on the process with ID **2680**, information about this process is listed on panel number **4**.

![](https://letsdefend.io/blog/wp-content/uploads/2021/01/Screen-Shot-2021-01-26-at-23.17.33.png)

With the "**More Info**" button on this panel, a page with detailed information about the process is opened. When we want to reach detailed information, we can use this section.

When the process information with 2680 ID is examined, the malware:

-   Uses Task Scheduler,
-   Writes a program to the file system which compile time is too old,
-   Writes many files to the user directory

![](https://letsdefend.io/blog/wp-content/uploads/2021/01/Screen-Shot-2021-01-26-at-23.25.05.png)

When we examine the process with ID **2616**, we see that it is **schtasks.exe** belonging to **Task Scheduler**.

When we examine the "**Command Line**" parameters, we see that it creates a schedule task named "**Updates\neHneiobyhcrJJ**". The configurations for this schedule task are in the file "**tmp5383.tmp**".

![](https://letsdefend.io/blog/wp-content/uploads/2021/01/Screen-Shot-2021-01-26-at-23.29.26.png)

When we examine the schedule task configuration file named **tmp5383.tmp**, we see that the program named "**neHneiobyhcrJJ.exe**" will run.

![](https://letsdefend.io/blog/wp-content/uploads/2021/01/Screen-Shot-2021-01-26-at-23.32.53.png)

When we examine the process with ID **3140**:

-   This malware is recognized by AnyRun as **AgentTesla**,
-   Steals credentials,
-   Creating files in the user directory

![](https://letsdefend.io/blog/wp-content/uploads/2021/01/Screen-Shot-2021-01-26-at-23.36.06.png)

When we examine the network connections made from panel number 3, we see that malware connects to **smtp.godforeu.com**.

With the help of the button on the right of the panel, we can examine the incoming/outgoing data.

![](https://letsdefend.io/blog/wp-content/uploads/2021/01/Screen-Shot-2021-01-26-at-23.39.10.png)

When the network activities of the malware are examined, we find that malware exfiltrates data with the SMTP protocol.

If you want to examine, you can reach the analysis made [here](https://app.any.run/tasks/e4979ab7-3145-4121-a042-ea91d7e2c86b).
