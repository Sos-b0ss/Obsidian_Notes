Sources:
https://sectools.org/tool/wapiti/
\
Wapiti allows you to audit the security of your web applications. It performs "black-box" scans; i.e., it does not study the source code of the application but will scans the webpages of the deployed webapp, looking for scripts and forms where it can inject data. Once it gets this list, Wapiti acts like a fuzzer, injecting payloads to see if a script is vulnerable.