# winpeas (.exe)
windows privilege escalation checklist with winpeas binary for windows

# download binary
[binary](https://github.com/alien-keric/winpeas/blob/main/winpeas.exe) - you can download the binary from this link

WinPEAS is a script that search for possible paths to escalate privileges on Windows hosts. The checks are explained on [book.hacktricks.xyz](https://book.hacktricks.xyz/windows-hardening/windows-local-privilege-escalation)

# parameter examples
```
winpeas.exe -h # Get Help
winpeas.exe #run all checks (except for additional slower checks - LOLBAS and linpeas.sh in WSL) (noisy - CTFs)
winpeas.exe systeminfo userinfo #Only systeminfo and userinfo checks executed
winpeas.exe notcolor #Do not color the output
winpeas.exe domain #enumerate also domain information
winpeas.exe wait #wait for user input between tests
winpeas.exe debug #display additional debug information
winpeas.exe log #log output to out.txt instead of standard output
winpeas.exe -linpeas=http://127.0.0.1/linpeas.sh #Execute also additional linpeas check (runs linpeas.sh in default WSL distribution) with custom linpeas.sh URL (if not provided, the default URL is: https://raw.githubusercontent.com/peass-ng/PEASS-ng/master/linPEAS/linpeas.sh)
winpeas.exe -lolbas  #Execute also additional LOLBAS search check
```
