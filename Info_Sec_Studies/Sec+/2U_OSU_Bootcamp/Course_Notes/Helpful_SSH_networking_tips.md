 You need a public facing port to connect to.

A good solution is [[Info_Sec_Studies/Sec+/Security+_Definitions/ngrok]] , search "[[tcp tunnel]]" you want [[Info_Sec_Studies/Sec+/Security+_Definitions/ngrok]] [[TCP]] 22.

It exposes the port to its own temporary [[domain]] name that is public facing. 
[[Info_Sec_Studies/Sec+/Security+_Definitions/ngrok]] is free, though the free users have their [[domain]] reset when [[Info_Sec_Studies/Sec+/Security+_Definitions/ngrok]] closes. 
Putting the computer to sleep doesn't close down [[Info_Sec_Studies/Sec+/Security+_Definitions/ngrok]]. 
Just don't close down [[Info_Sec_Studies/Sec+/Security+_Definitions/ngrok]] and you should be fine.

The other option I have done is to buy a [[host]], ([[domain]] optional) (I use [[digitalocean]], and [[namesilo]]), 
then use [[tinc]] to [[VPN]] my home computer, my server, and my laptop with my server as the host and the other two computers as clients. 
I then [[SSH]] to my [[Server]], then I can [[SSH]] to my other computer. 

Website the tip is found:
http://askubuntu.com/questions/749230/ddg#1002532
