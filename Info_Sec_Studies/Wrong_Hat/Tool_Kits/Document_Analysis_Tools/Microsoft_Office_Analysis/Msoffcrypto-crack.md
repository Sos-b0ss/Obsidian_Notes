Sources:
https://blog.didierstevens.com/2018/12/31/new-tool-msoffcrypto-crack-py/
\
This is a new tool to recover the password of encrypted MS Office documents. I quickly put together this script to help with the analysis of encrypted, malicious documents.

This tool relies completely on Python module [msoffcrypto](https://github.com/nolze/msoffcrypto-tool) to decrypt MS Office documents.

Since this is a Python tool based on a Python library, don’t except fast password recovery. This is more a convenience program.

It can recover passwords using a build-in password list, or you can provide your own list via option -p.

The tool can also decrypt the encrypted MS Office document if the password is recovered: used option -o to achieve this. Otherwise, the tool just displays the recovered password.

Like many of my tools, it can take its input from stdin and provide the decrypted document via stdout.

It’s developed with Python 2, and also tested on Python 3.
