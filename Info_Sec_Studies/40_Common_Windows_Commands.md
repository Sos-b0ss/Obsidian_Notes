
To get a condensed list of the device's [[IP]] information:
```
ipconfig
```
\
To get all the device's [[IP]] information, [[MAC]] address and [[DNS]] info:
```
ipconfig /all
```
\
To use what is similar to [[Grep]] in [[Linux]]:
```
ipconfig /all | findstr <arg>
```
\
To get a new [[IP]] address on the system from the [[DHCP]] server you can use:
```
ipconfig /release
ipconfig /renew
```
\
However if you dont want to refresh all the interfaces you can specify which inteface with:
```
ipconfig /release "Wi-Fi"
```
\
To troubleshoot any [[DNS]] problems because 9 times out of 10 the problem is here:
```
ipconfig /displaydns
```
\
Because that is very verbose you can instead just copy everything to your clipboard so that you can transfer it somewhere a bit more easy to read:
```
ipconfig /displaydns | clip
```
\
To delete your [[DNS]] resolver [[Cache]] you can run:
```
ipconfig /flushdns
```
\
To troubleshoot [[DNS]] problems even further you can use the command:
```
nslookup google.com
```
\
You can also specify a different [[DNS]] server that you would like to use while troubleshooting:
```
nslookup google.com 8.8.8.8
```
\
You can also look for other types of [[DNS]] records with:
```
nslookup -type=mx google.com
nslookup -type=txt google.com
nslookup -type=ptr google.com
```
\
To clear your screen use:
```
cls
```
\
To get all your [[MAC]] addresses for your device use:
```
getmac /v
```
\
This is something you can use to check if there is any power issues with your system:
```
powercfg /energy
```
\
To check any issues with your battery if you have one connected use:
```
powercfg /batteryreport
```
\
To check which file types are associated with which programs on your system use:
```
assoc
```
\
If you want to change the program that is used by default to open a certain file type you can use:
```
assoc .mp4=VLC.vlc
```
\
To check if theres any errors in your disk and run a repair on them use:
```
chkdsk /f
```
For physical sector issues on your disk instead use:
```
chkdsk /r
```
\
To use system file checker to see if there are any issues with .[[dll]] files if both of the chkdsk options didnt fix your issues:
```
sfc
```
\
If youre still having issues you may need to instead use deployment service imaging and management, this will actually use the internet to fix your system image:
```
DISM /Online /Cleanup-Image /CheckHealth
```
\
For an even deeper scan using this tool you can:
```
DISM /Online /Cleanup-Image /ScanHealth
```
\
If there are some bad issues that is being picked up by the check or scan use:
```
DISM /Online /Cleanup-Image /RestoreHealth
sfc /scannow
```
\
To fix when someone manages to use a bad [[USB]] on your system:
```
tasklist | findstr script
```
\
Now with the process ID ([[PID]]) of the malicious program or script thats running you can kill it with:
```
taskkill /f /pid <PID>
```
\
A more useful tool similar to ipconfig that will show you more information in a written report and even suggested commands to run to fix these issues:
```
netsh
netsh wlan show wlanreport

## To show your interfaces:
netsh interface show interface

## To show you your IP addresses:
netsh interface ip show address | findstr "IP Address"

## To show you your DNS servers:
netsh interface ip show dnsservers

## To turn off the windows defender firewall:
netsh advfirewall set allprofiles state off
or on:
netsh advfirewall set allprofiles state on
```
\
To check if a server or website is up or if your system is able to make a connection to it:
```
ping google.com

## To do this but not have it time out use:
ping -t google.com
```
\
To see if the route to the destination address has any connection problems use:
```
tracert google.com

## To run the same command but not resolve domain names to save time:
tracert -d google.com
```
\
To see what youre connecting to and what is connected to you use:
```
netstat

## To see what ports are currently open on your system use:
netstat -af

## To see all the process IDs for all the connections use:
netstat -o

## To get your sending and recieving statistics use (every 5 sec):
netstat -e -t 5
```
\
To see all the routes (Gateways) your system will take to get to your connections (Your systems routing table): 
```
route print

To add routes to your computer use:
route add <dest ip addr> mask 255.255.255.0 <thru ip addr>
ex.
route add 192.168.40.0 mask 255.255.255.0 10.7.1.44 

To delete routes use:
route delete <route dest ip addr>
ex.
route delete 192.168.40.0
```
\
To shutdown your computer or restart it into the system bios use:
```
shutdown /r /fw /f /t 0

If you just need to shut it down use:
shutdown
```
