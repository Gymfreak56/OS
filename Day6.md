## Process Validity
```

Making sure processes are legitimate. 
process is just code that gets run

dll - stand alone program(not directly executed)

```

## Service
```

processes that run in the background
services.mse -- 

get-ciminstance win32_service
Get-CimInstance win32_service | Select-Object name,processid,pathname | more
get-service

sc query
sc queryx type=service -- extended 

```

## DLL
```

get-process chrome | ForEach-Object {$a} {$_.modules} | more -- see dll's that 
Get-Process -name "*chrome*" | Select-Object -ExpandProperty modules | more
Get-Process chrome | ForEach-Object {$a} {$_.modules} | Where-Object modulename -like '*chrome*' | more -- grabe files or modules that have chrome in the name.

tasklist /m -- modules
tasklist /m /fi "imagename eq chrome.exe"
tasklist /fo:(list,table,csv)

```

## Processes
```

get-ciminstance win32_process | select-object name, processid, parentprocessid | sort-object id -- get parent process id's

```

## Scheduled Tasks
```

GUI -- Task Scheduler

get-scheduledtask | select-object * | select-object -first 1

schtasks /create /tn random /sc minute /mo 15 /tr "powershell.exe -win hidden -encode jhcvefvl"
schtasks /query | select-string -pattern random -context 2,4

get-scheduledtask | select * | select-string -pattern random -context 2,4


```

## Network connections
```

get-nettcpconnection
Get-NetTCPConnection -state Established

netstat /antp -- /ano

```

## User Access Control
```

colors == Red, Blue&Gold, Blue, Yellow
comes from a manifest file

runlevels

asinvoker -- perms of user

required admin -- needs to be admin

Highest Available -- highest perms you have

```

## sysinternals
```
collection of tools

cd .\sysinternalssuite\
.\sigcheck.exe -m C:\windows\regedit.exe
.\strings.exe -s C:\windows\system32\*.exe | findstr /i autoelevate -- finds executables with autoelevate on

net use * http://live.sysinternals.com
cd (DRIVE) -- online version

$wc = New-Object system.net.webclient
PS C:\> $wc.downloadfile("https://download.sysinternals.com/files/sysinternalssuite.zip")

```

## Exploit
```

fodhelper.exe
calls on registry keys that dont exist so he added it with malicious code


```

## procmon
```

enable bootlogging -- captures processs as system boot up.

UAC

HKLM\Software\microsoft\windows\currentversion\run

```

## autoruns
```

shows applications that automatically start at boot


```

## procexp(process explorer)
```

Real time.

```

## TCPVIEW
```

netstat

```

## PSEXEC
```

commmandline
run in powershell 
psexec /?
psexec -i -s regedit.exe == interactive

```

## logonsessions
```

logonsessions.exe -accepteula -p | more -- shows who logged on and how

```

## psloggedon
```



```

## pslist.exe
```

pslist -s 100 -r 10 -- runs for 100 seconds, refreshes every 10 seconds

```

## psinfo
```

info on local machine info(can be run remotely)


```

## strings
```

strings -a C:\users\andy.dwyer.desktop\newdoc.txt
strings -a -- pulls out human readable text (ASCII) from a file 

```

## handle
```

tracked in object manager
start-transcript
get-process | whre-object {$_.name -contains "powershell"}

handle.exe -p 3200 -accepteula 

get-process | whre-object {$_.name -contains "*.txt"}

handle -p id -c C:\users\and.dwyer\documents\powershell_transcript

```

##Firewall
```

netsh advfirewall show allprofiles

```

## AccessChk 
```

windows prmissions

```

