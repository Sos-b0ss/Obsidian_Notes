# Q1:
A security engineer would like to determine if attackers are trying to gain access to the company's network, and if they were to gain access, what actions they would perform. As a way to address this, the engineer has developed an area of the network that houses no important or private information. Instead, the portion of the network is filled with dummy resources and analysis tools. The goal is that an attacker will not be able to determine which resources are valid and which are fake. If the attacker performs any actions on the decoy network, the security engineer will be able to analyze the actions taken to ensure better protection in the future.

What is the section of the network that houses the dummy resources known as?

What did I answer?:
**Decoy zone (DCZ)**

Correct answer: **Honeynet**

A honeypot is a single resource created to look like a legitimate resource with the goal of tricking an attacker. A section of the network which contains multiple honeypots, or decoy systems, is known as a honeynet.

The demilitarized zone (DMZ) of a network is a zone that houses servers that must be accessible over the internet. **Dummynet and decoy zone are fabricated terms.**

# Q2:
You have been tasked with implementing controls to help with data loss prevention (DLP) within your organization.

Of the following options, which would be the BEST to assist in data loss prevention?

What did I answer?:
**Stateful firewalls**

Correct answer: **USB blocking**

Data loss prevention (DLP) is meant to stop the leakage of confidential data. While all of the options mentioned are useful to improve the overall security of an organization, USB blocking is the best option to directly address data loss prevention specifically.

# Q3:
HMAC can be described as which of the following?

What did I answer?:
**Key stretching algorithm**

Correct answer: **Hashing algorithm**

HMAC, which stands for Hash-based Message Authentication Code, is a type of hashing algorithm. Other hashing algorithms include Message Digest 5 (MD5), Secure Hash Algorithm (SHA), and RACE Integrity Primitives Evaluation Message Digest (RIPEMD).

# Q4:
Of the following cloud deployment models, which provides an entire cloud computing platform that allows developers to quickly jump in and develop applications?

What did I answer?:
**IaaS**

Correct answer: **PaaS**

Platform as a service (PaaS) is a cloud development model that provides an entire cloud computing platform for developing applications. PaaS allows developers to focus on creating and managing their applications without having to deal with managing the hardware and operating systems. In many cases, the PaaS provider even installs the necessary updates and patches to the operating system.

# Q5:

An attacker had access to a virtual machine. With access to the virtual machine, the attacker was able to run code on the virtual system and access the hypervisor. Having control over the hypervisor, the attacker had complete control over all of the virtual machines on the host.

What is the name of this type of attack?

What did I answer?:
**VM sprawl**

Correct answer: **VM escape**

A VM escape is an attack in which the attacker can access the underlying host system. The host system runs an application known as a hypervisor. The hypervisor manages the virtual machines on the host system. In some cases, the attacker can run code on the virtual machines and access the hypervisor and host system.

# Q6:
The programs Bycrypt and PBKDF2 are both examples of what type of technology?

What did I answer?:
**Encryption Algorithm**

Correct answer: **Key stretching**

Key stretching (also known as key strengthening) takes a weak key and attempts to strengthen it by increasing its size. The purpose of key stretching is to make password attacks, such as brute force attacks, more difficult. Bycrypt and PBKDF2 are both examples of key stretching programs.

# Q7:
What type of cipher is the Triple Data Encryption Standard (3DES)?

What did I answer?:
**Asymmetric block cipher**

Correct answer: **Symmetric block cipher**

3DES, pronounced Triple DES, was built as an improvement over the Data Encryption Standard (DES). Both DES and 3DES are symmetric block ciphers. Symmetric encryption uses the same key to encrypt and decrypt data, while asymmetric uses two keys in a matched pair for encryption and decryption. A block cipher encrypts data in blocks (such as 64- or 128-bit blocks), while a stream cipher encrypts it as a stream of bits.

---
# Study
Below are questions I had flagged in my practice exams but got correct, Write out why I would be unsure about what the answer is and the correct answer in my own words that makes sense to me.

---

You would like to incorporate a program that uses both symmetric and asymmetric encryption to increase the security of e-mail communication.

Which of the following should you use?

Correct answer: PGP

Pretty Good Privacy (PGP) is a method used for securing email communications. PGP can encrypt, decrypt, and digitally sign email messages. PGP utilizes both symmetric and asymmetric encryption.

AES (Advanced Encryption Standard) and Blowfish are both examples of symmetric algorithms. RSA (Rivest, Shamir, Adleman) is an asymmetric algorithm.

---

You are taking an approach of security through obscurity.

Which of the following is an example of this concept?

Correct answer: Obfuscation

Security through obscurity is a security concept which asserts that by making something harder to find or more difficult to understand, it will be secure. Obfuscation is a technique for making something harder to understand. For example, code obfuscation refers to adding nonsense and extra information into the code to throw an attacker off track. It should be noted that most security professionals reject security through obfuscation as a reliable method for maintaining security.

---

Which of the following biometric methods uses the pattern of blood vessels behind the eye for recognition?

Correct answer: Retina scanner

Two types of biometrics scanners involve the eyes: retina scanners and iris scanners. The retina scanner uses the pattern of blood vessels in the back of the eye for recognition.

Iris scanners capture an image of the iris around the pupil for recognition. Cornea scanner and pupil scanner are both fabricated terms.

---

Which of the following would NOT technically be considered multifactor authentication (MFA)?

Correct answer: Password and security questions

Multifactor authentication (MFA) is when two or more types of authentication factors are in place. Types of authentication factors include something you are (biometrics), something you have (hardware token), something you know (PIN, password, security questions), somewhere you are (location-based), and something you do (behavior-based).

Password and security questions are the same type of authentication factor - something you know. Although some organizations may believe this is multifactor authentication, that is technically incorrect.

---

You have implemented a biometric authentication system for your organization. One day, you found that the biometric system allowed an individual into the building that should not have been allowed to enter.

What is this an example of?

Correct answer: False acceptance

Failures in which a biometric system improperly categorizes people include false acceptance and false rejection. A false acceptance occurs anytime an individual that should not be allowed access is granted access.

A false rejection occurs when a user is denied access even though they should be allowed access. A positive acceptance refers to when a user who should be allowed access is accurately granted access. A positive rejection refers to when a user who should not be allowed access is accurately rejected access. Positive acceptance and positive rejection happen when the system is working properly.

---

You are working on a software development project. You know that there are multiple software development lifecycle (SDLC) models that can be used. In the model that is being used for this project, there are multiple stages that go from top to bottom. Each stage feeds into the next stage. Some of the stages include requirements, design, implementation, verification, and maintenance.

Which SDLC model is being used here?

Correct answer: Waterfall

The waterfall model uses a methodology that includes multiple stages, all of which feed into each other. When you finish one stage, you move onto the next stage. It is named waterfall because the stages start at the top and flow into each other.

---

You are in the process of implementing a new virtual environment for an organization. You have chosen to go with a hypervisor that runs directly on the system hardware.

What type of hypervisor did you choose?

Correct answer: Type I

A type I hypervisor, also known as a bare-metal hypervisor, runs directly on system hardware. A type II hypervisor runs as software inside of a system's operating system.

Type III and type IV are fabricated.

---

You are working as a network engineer for a consulting company that has both government and non-government clients. Because the data relating to government clients is classified and controlled, the entire network that handles that data is physically isolated from the network that handles non-government clients.

What is the name of this technique?

Correct answer: Air gap

An air-gapped network means that the network is not connected to any other network and therefore completely isolated. The term air gap is synonymous with physical isolation. It implies that there is a gap of air between one system (or network) and another. Air gap techniques can be employed against a single component, system, or entire network.

---

Of the following, which is another name for a type I hypervisor?

Correct answer: Bare-metal

A type I hypervisor runs directly on a system's hardware rather than running inside the system's operating system like a type II hypervisor. Since the hypervisor doesn't require the operating system to run, it is often referred to as a bare-metal hypervisor. It is also considered a "native" hypervisor rather than a "hosted" hypervisor.

---

You are a systems administrator. You have been tasked with protecting the password stored in the shadow password file on a Linux machine.

Which of the following can be used to complete this task?

Correct answer: Bcrypt

Bcrypt is a tool that can be used to perform key stretching. Key stretching is a security technique that increases the strength of stored passwords. Bcrypt is based on the Blowfish block cipher.

---

Which of the following is a cryptographic hashing function?

Correct answer: SHA

The Secure Hash Algorithm (SHA) is the only option listed that is a hashing function. Hashing functions are used to generate a hash (a summary of a file or message) which is then used to verify the integrity of the data.

Diffie-Hellman (DH) is a key exchange used for establishing a shared key. Data Encryption Standard (DES) and Advanced Encryption Standard (AES) are encryption algorithms and not hashing functions.

---

Of the following, which is the LEAST reliable concept for ensuring security within a network?

Correct answer: Security through obscurity

Security through obscurity is a concept that asserts something will be secure if it's hidden or difficult to understand. Code obfuscation is an example of security through obscurity. Security through obscurity is considered a weak defense and should not be used as a primary security method.

Defense in depth is a concept in which the more security controls are in place, the better. The principle of least privilege outlines that users, processes, and applications should all have the bare minimum of permissions to operate. SecDevOps is a concept that integrates security into every phase of software development.

---

You are in the process of implementing a new hypervisor for your virtual environment. The hypervisor runs as software within the system's operating system.

Which type of hypervisor is being described in this scenario?

Correct answer: Type II

A type II hypervisor is one that runs as software on a system's operating system. Virtualbox is an example of a type II hypervisor.

A type I hypervisor is one that runs directly on a system's hardware. Type I hypervisors are also referred to as native and bare-metal hypervisors.

---

