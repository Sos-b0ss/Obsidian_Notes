Sources:
https://youtu.be/WfYxrLaqlN8

sudo dpkg-reconfigure [[Wireshark]]-common
\
sudo [[usermod]] -a -G [[Wireshark]] {your username}

---------------------------------------------------------------------------------
Aircrack - ([[Airmon]])
\
sudo apt-get install [[realtek]]-rtl88xxau-dkms
\
sudo [[airmon-ng]] check kill
\
sudo [[airmon-ng]] start wlan0

---------------------------------------------------------------------------------
\
[[Aircrack]] & [[Airodump]]:
\
this is for 2.4ghz:
sudo [[airodump-ng]] wlan0
\
this will pull everything from 5ghz too:
\
sudo airodump-ng -b a wlan0
\
if you click [a] you can change the filter to see stations connected to the access points
\
the names of [[Probes]] are showing you the names that devices like phones and computers are looking out for a router named that
\
if you see any devices that are "not associated", and you change your Wi-Fi adapters name to the probe name their device will connect to you as a Wi-Fi connection, and this is the heart of an evil twin attack.
\
these commands are found in [[Aircrack]] when you choose the suite that you are using.
\
if you click [tab] while in the access points view it will color-code points of interest for scan 
\
you can mark them with [m] when you select it with arrow keys. When you go to the stations view you can now see a correlation between points of interest and stations.

---------------------------------------------------------------------------------

aircrack [[Air-Replay]]:
\
sudo aireplay-ng -0 25 -D -a *router mac address* *name of your wifi adapters name*
\
-0 is [[Deauth_Attack]] | 25 is the [[Packet]] amount | -D is making it so it doesn't check for what channels devices are connecting to | -a is [[Access_Point]] | you can put -c after the [router [[MAC]]address to just disconnect one [device mac address]
\
this is important because you can capture a [[WPA_Handshake]]] during the devices auto-connect using [[AiroDump]].
\
now with this you can use [[AirCrack]] and use the [[WPA]] handshake and it will start cracking the [[WIFI]] routers password
\
to make a fake access point use:
\
sudo [[airbase-ng]] -C 60 -P [[Wifi_Adapter]] name]
\
-C is for change and the 60 is the amount of seconds the broadcast is for | the -P is making the fake wifi whatever the name of the probes devices are looking for
\
[[MacChanger]] can be used to change your mac address to whatever 
\
this can be used for evil twin, can be used for getting onto hotel wifi networks, airport networks, once you can capture that [[WPA_Handshake]] and crack it you can get the password, and then you can also just kick off a device and change your [[MAC]] address to the [[MAC]] address the router is looking for.
\
tools to make this all work:
- [[Fern]]
- [[Wifite]]
- [[AirCrack]]
- [[Ettercap]]/[[Bettercap]]
\
when and if you ever do this you should always change the mode your wifi adapter is working in from monitor to managed.
\
[[nmap]] --script vuln *ip addr*
\
When using [[Wireshark]] and if you want to narrow the filter to just look for [[ARP handshakes]] you can use:

- [[arp.opcode]] == 1 [Tells you what devices are asking for MAC addresses] 
- [[arp.opcode]] == 2 [Tells you what devices are providing MAC addresses]

The 2 are super helpful 
\
Other tools to research for similar effects:
- [[Arpspoof]] *[[kali]]*
- [[Ettercap]] or [[Bettercap]] *Linux*
- [[Caine_and_Abel]] *Windows (slightly sus and VERY old)*
