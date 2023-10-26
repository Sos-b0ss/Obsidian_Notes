Steps:

quick tidbit if you're still somehow having issues  
  
deactivate anti-virus as needed, or whitelist download location  
Download torrent  
Disable internet adapter or activate network lock  
unpack & install per torrent instructions (license file literally gets drag and drop to running client, not file to folder... while app is running, just pull the license to it. boom. it's activated.)  
  
Once activated offline, disable updates in app preferences  
in your firewall of choice, block the following;  
ableton index.exe  
ableton live 10 suite.exe  
ableton web connector.exe  
installerhelper.exe  
(should all be in install folder/subs, default ./programdata/ableton/live 10 suite)  
turn on internet  
profit  
  
gotten no outbound/inbound traffic to app, no nag about activation

---

If anyone else also keeps getting the invalid auth file, here's what you do:  
  
To unflag your PC, you have to do this:  
  
  
  
Open regedit and go to;  
  
Computer\HKEY_CLASSES_ROOT\ableton  
  
AND  
  
Computer\HKEY_CURRENT_USER\Software\Ableton  
  
AND  
  
Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Ableton  
  
  
  
Delete all folders called Ableton  
  
  
  
And then go to these folders, and delete all folders called Ableton  
  
C:\Users\User\Documents  
  
C:\Users\User\AppData\Local  
  
C:\Users\User\AppData\Roaming  
  
  
  
Then disconnect from the internet. Reinstall Ableton as usual  
  
Inside Ableton, go to Options > Preferences > License Management  
  
Turn off auto updates  
  
Then drag and drop your .auz file inside Ableton. It should work now

