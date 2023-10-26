[[echo]] ea847988ba59727dbf4e34ee75726de3 > hash.txt
[[Cat]] hash.txt 
[[Hashcat]] -m 0 -a 0 -o solved.txt hash.txt /usr/share/[[wordlist]]s/[[rockyou.txt]] --force
[[Sudo]] [[Hashcat]] -m 0 -a 0 -o solved.txt hash.txt /usr/share/[[wordlist]]s/[[rockyou.txt]] --force
\
This can do everything john could do however its slightly more efficient and can also actually use [[rainbow tables]].
