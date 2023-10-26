[[Port_Forward]]ing so as to be able to pivot without [[Metasploit]]:
\
```
netsh interface portproxy add v4tov4 listenport=XXXX listenaddress=Y.Y.Y.Y connectport=ZZZZ connectaddress=T.T.T.T
```
