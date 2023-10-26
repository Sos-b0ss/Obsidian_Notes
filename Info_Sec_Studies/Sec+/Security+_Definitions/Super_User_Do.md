Sources:

\
Used in [[Linux]] [[OS]] when you need to access or make changes to a file or directory within the [[Terminal]] but with the elevated permissions of a super user.
ex. 
```
sudo mv /home/jenny/example.txt /home/adam/example.txt
```
\
These users are able to have as much power as the root user without actually being the root user, because this is the case it's highly important to think twice before running something on a system with [[Sudo]] and minimize the amount of users that have access to this group to as little as possible.
