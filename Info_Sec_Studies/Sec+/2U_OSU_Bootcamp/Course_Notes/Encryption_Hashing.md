

[[Sec+ Encryption]]
[[Career/Oops_Dups_Archive/Professor_Messer/Hashing]]

[[Career/Oops_Dups_Archive/Professor_Messer/Hashing]] is NOT [[Career/Oops_Dups_Archive/Professor_Messer/encryption]]

because hashing is not reversible - only ONE WAY

hashes are stored in [[/etc/shadow]] dir

pass_crackers do not unhash passes

[[john the ripper]] | [[hash cat]] | [[Hydra]]
the format to crack using these tools
(
name:hash
name:hash
name:hash
)
* = no pass
! = disabled user

[[john]] listname.txt -wordlist =/usr/share/wordlist/.txt
	--show will show you what the hashes mean

[[usermod]] -aG [[Sudo]] {user} -to change group
[[/etc/sudoers]] <- to see all super users
in less using !bash gives [[root]] priv.

system users always have a [[uid]] >1000 (these are automatically generated)
standard users have a [[uid]] <1000 (users you create)
root uid is 0

[[Sudo]] [[deluser]] --remove-home {user}
^^^
(removes home dir)

linux uses [[DAC]] (discretionary access)
-rw-r--r--

you can change file perms symbol or [[octal]](with #s)

rwx rw- r--
421 420 400
|7| |6| |4|

so you would use [[chmod]] 764 {filename}

ls -l to show file perms
[[Sudo]] -l to see what [[Sudo]] perms user has

[[samba]] ([[smd]]) is a file sharing protocol allows users to view, download, and store files remotely

new tools -> [[chkrootkit]],[[lynis]]
[[systemctl]] -r --all <- list all services on system
[[systemctl]] {[[Services]]} {start,stop,remove,disable}