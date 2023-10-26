Sources:
https://sectools.org/tool/socat/
\
 [socat](http://www.dest-unreach.org/socat/) is a very powerful command-line tool which will enable you to forward ports and a lot more. Here is a sample usage:
\
```
socat -d -d tcp4-listen:XXXX,reuseaddr,fork,tcpwrap=socat tcp4:T.T.T.T:ZZZZ
```
