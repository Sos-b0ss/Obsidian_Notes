Sources:
https://en.wikipedia.org/wiki/Birthday_attack
https://www.geeksforgeeks.org/birthday-attack-in-cryptography/
\
A birthday attack is a type of cryptographic attack that exploits the mathematics behind the birthday problem in probability theory. This attack can be used to abuse communication between two or more parties.
\
An example of using a [[Hash_Collision]] to reveal the secret.
\
When two [[Hash]]es share the same data
\
One way to avoid hash collision is to increase the sample size of options you're [[Hash]]ing.
\
Ex.
- Assuming a non leap year(hence 365 days).   
- Assuming that a person has an equally likely chance of being born on any day of the year.   
- Let us consider n = 2.   
- P(Two people have the same birthday) = 1 – P(Two people having different birthday)   
                                                              = 1 – (365/365)*(364/365)   
                                                              = 1 – 1*(364/365)   
                                                              = 1 – 364/365   
                                                              = 1/365.   
\
So for n people, the probability that all of them have different birthdays is:   
P(N people having different birthdays) = (365/365)*(365-1/365)*(365-2/365)*….(365-n+1)/365.   
                                                              = 365!/((365-n)! * 365n)
\
**Algorithm:**
1.  Choose 2n/2 random messages in M: m1, m2, …., mn/2
2.  For i = 1, 2, …, 2n/2 compute ti = H(mi) => {0, 1}n
3.  Look for a collision (ti = tj). If not found, go back to step 1
