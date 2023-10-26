Sources:
https://blog.didierstevens.com/programs/pdf-tools/
\
This tool is not a PDF parser, but it will scan a file to look for certain PDF keywords, allowing you to identify PDF documents that contain (for example) JavaScript or execute an action when opened. PDFiD will also handle [name obfuscation](https://blog.didierstevens.com/2008/04/29/pdf-let-me-count-the-ways/).
\
The idea is to use this tool first to triage PDF documents, and then [analyze the suspicious ones with my pdf-parser](https://blog.didierstevens.com/2008/10/20/analyzing-a-malicious-pdf-file/).
\
An important design criterium for this program is simplicity. Parsing a PDF document completely requires a very complex program, and hence it is bound to contain many (security) bugs. To avoid the risk of getting exploited, I decided to keep this program very simple (it is even simpler than pdf-parser.py).
