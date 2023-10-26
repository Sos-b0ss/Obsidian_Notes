Sources:

\
[[Head]] - Top 10 lines of the file (by default)
[[Tail]] - Bottom 10 lines of the file (by default)
[[Less]] - views file 1 page at a time (scroll)
[[More]] - views file 1 page at a time (space)
[[OSI-RM]] - remove
[[PWD]] - print working directory
[[Cat]] - combines two files into one viewing
[[Stdin_&_Stdout]] - to redirect data streams (Standard in -> Standard out)
ex.
	``">" will overwrite a file, ">>" will append a new file``
	``cat 1.txt 2.txt > Combined_1_and_4.txt`` (**this will override**)
	``cat 3.txt 4.txt >> Combined _3_and_4.txt`` (**this will append on the bottom**)

[[SED]] - reads & edits text from input stream
[[AWK]] - away to delineate data from a stream
ex.
	``awk -F, '{print & (field_number)}'``

[[Nano]] - base text editor usually always included in [[Linux]] distributions
[[Cut]] - substituting text/filtering lines of text/delineating text
[[Sed_Syntax]] - sed s/old value/new value/

\
ex.
``awk -F'(filed separator)' '{print $1,$6,$9}' /etc/passwd``
\
**awk notes:**
	-F = [[Flag]] used to make [[AWK]] execute '[[Field_Separation]]'
	Whats after -F is the [[Parameter]] which signifies what separates the data also known as the [[Deliminator]]

**Benefits of scripting:**
- Consistency
- re-usability
- efficiency

**In shell scripting there are different shells to be used:**
-[[Sh]]
-[[Bash]]
-[[Zsh]]
-[[Csh]]

**Other Helpful tools to use while in the Terminal:**
[[Top]] - 
[[PS]] - [[psaux]] (A-all services U-active user X-all processes w/ no terminal) keep this all lowercase if you want to live.
[[Kill]] - Using this command and supplying it with a [[Process_ID]] or [[PID]]
