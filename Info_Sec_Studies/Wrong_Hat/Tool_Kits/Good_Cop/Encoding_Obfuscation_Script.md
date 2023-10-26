Sources:
https://www.youtube.com/watch?v=bdoINmJFw3M
https://github.com/moom825/batch-obfuscator-made-in-python
\
Here's a very strange technique some malware authors may try and use as a form of obfuscation written in python. This will change the encoding of the text in the file to show up as foreign characters however the script will still run without being effected.
\
**Obfuscation code:**

```
@echo off
if "%-1"=="" exit /b
if /i "%-x1" neq ".bat" if /i "%-x1" neq ".cmd" exit /b
for /f %%i in ("certutil.exe") do if not exist "%%-$path:i" (
	echo CertUtil.exe not found.
	pause
	exit /b
)
>"temp.-b64" echo(//4mY2xzDQo=
certutil.exe -f -decode "temp.-b64" "%-n1o%-x1"
del "temp.-b64"
copy "%-n1o%-x1" /b + "%-1" /b
```

**De-Obfuscation code:**


```
@echo off
if "%-1"=="" exit /b
if /i "%-x1" neq ".bat" if /i "%-x1" neq ".cmd" exit /b
if exit "%-n1___%-x1" del "%-n1___%-x1"
for /f "skip=1 delims=" %%L in ('CMD /U /C Type "%-1"') do (
	echo %%L
	echo %%: >>"%-n1___%-x1"
)
pause>nul
```
