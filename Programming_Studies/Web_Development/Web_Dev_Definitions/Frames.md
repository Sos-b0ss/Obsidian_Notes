Source:
https://www.techtarget.com/searchnetworking/definition/frame
\
In telecommunications, a frame is data that is transmitted between network points as a unit complete with addressing and necessary protocol control information. A frame is usually transmitted serial bit by bit and contains a header field and a trailer field that "frame" the data. (Some control frames contain no data.)
\
One way to define frames in networking is that the frame is a primary data unit within Level 2, or the data link layer of the OSI model. By contrast, Level 3, or the networking layer of the OSI model uses the packet as a primary data unit.
\
Frames and packets may have different terminology attached to their use depending on the context or industry in question. In general, the frame is a formatting resource for data that needs to be split up into recognizable pieces in order to be interpreted by a receiver.
\
--------Header-------................................................................----------Trailer---------

| Flag (01111110) | Address field | Information (data) field (0-4096 bytes) | Frame check sequence | Flag (01111110) | 
| --------------- | ------------- | --------------------------------------- | -------------------- | --------------- |
