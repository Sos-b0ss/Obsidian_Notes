Sources:
https://www.youtube.com/watch?v=lxrF9FzxeTU
\
First came about in [[Windows]] Server 2012. It was supposed to be the next generation file system to replace [[NTFS]]. This file system can only be used with windows pro for workstations or enterprise. It also cant actually be used on a single drive, it needs to be used on a pool of drives using windows built in "Storage Spaces" feature.
\
Main features of [[ReFS]] is that it makes your file system more resistant to errors and corruption, so it increases fault tolerance. It also does automatic metadata integrity checking.
\
Using the commands:
```
Set-FileIntegrity "X:\foobar" -Enable $True
```
\
You're able to enable the ability to have windows check the file integrity rather than just the metadata which is enabled by default.
\
However if you're needing to enable this file integrity check for files that are already on the drive youll need to run this instead for each file that you need it enabled for:
```
Get-Item -Path 'X:\foo\bar' | Set-FileIntegrity -Enable $True
```
\
Every few weeks or so it also goes through a scheduled integrity check which is called "[[Scrubbing]]". But using task scheduler you can enable that to be more frequent.
\
Features that are only in the [[ReFS]] file system that aren't in standard file systems:
- [[Block_Cloning]]: Similar to "[[De-Duplication]]". Basic idea, whenever you make a copy of a file on the drive it will instead make a pointer to that original until changes are made and this helps save space on the drive. Uses "[[Copy-on-Write]]" to avoid any collisions when a file is being read and another program is writing to the pointer of that original file.
- [[Sparse-VDL]] ([[Valid_Data_Length]]): Primarily fixes issues with any disparity between a files allocated size and its actual data size which is called valid data length. This allows your drive to be used to make virtual machines much faster if that's what you're main use for the drive is.
	- See. https://tinyurl.com/2p8enfns
- [[Mirror_Accelerated_Parity]]: Essentially replicates the effect of having [[Raid]] 1 set up on your drive, so standard drive mirroring but a bit faster because it works around calculating the parity at a certain threshold rather than instantly which is what standard Raid-1 does.
- [[File_Level_Snapshots]]: Mainly applies to windows server, but its basically the same as windows' "file history" but its useable on the file level rather than where normally with an [[NTFS]] drive that windows server is using you would have to take a whole snapshot of the drive which is far more bulky and slow.
\
Drawbacks of [[ReFS]]:
- You cant boot an [[OS]] off an [[ReFS]] enabled drive.
- There's no native file system level compression, so you would NEED to use 3rd party programs to achieve this.
- Does not have native support of file level encryption so you cant have it encrypted automatically, but will still let you use things like [[bitlocker]] or other software level encryption programs.
- Cant have page file / [[Swap_Space]] on an [[ReFS]] drive. 
- Does not support being implemented on any removeable drives, it must be put on a permanent drive.
\
![[Pasted image 20220830125752.png]]
\
Above is a list of all the currently unsupported features.
