## Registry
```

regedit.exe -- GUI

reg.exe - CLI
reg add, reg query, reg delete

reg query hklm\software\microsoft\windows\currentversion\run
reg add hklm\software\microsoft\windows\currentversion\run/v testme /t REG_SZ /d C:\windows\system32\pindowspowershell\v1.0\powershell.exe
reg delete hklm\software\microsoft\windows\currentversion\run/v testme 

Powershell
get-item, get-itemproperty

get-childitem hklm:\software\microsoft\windows\currentversion\
get-item hklm:\software\microsoft\windows\currentversion\run
new-item 'hklm:\software\microsoft\office\14.0\security\trusted documents\trustedrecords' -force
new-itemproperty 'hklm:\software\microsoft\office\14.0\security\trusted documents\trustedrecords' -name "%userprofile%Downloads/test-document.txt"
new-itemproperty hklm:\software\microsoft\windows\currentversion\run -name Test -propertytype string -value C:\windows\system32\pindowspowershell\v1.0\powershell.exe
rename-itemproperty -path hklm:\software\microsoft\windows\currentversion\run -name SecurityHealth -newname Test
get-item hklm:\software\microsoft\windows\currentversion\run
remove-itemproperty 'hklm:\software\microsoft\office\14.0\security\trusted documents\trustedrecords' -name "%userprofile%Downloads/test-document.txt"
get-item 'hklm:\software\microsoft\office\14.0\security\trusted documents\trustedrecords'
remove-item -path 'hklm:\software\microsoft\office\14.0\security\trusted documents\trustedrecords' 

```

## PS Drive
```

get-childitem ENV:

mkdir demo
new-psdrive -name demo -psprovider filesystem -root C:\demo
cd demo:

get-childitem HKU:
New-PSDrive -name HKU -psprovider Registry -root HKEY_USERS
get-childitem HKU:

cd registry::hkey_Local_Machine
cd HKU
C:

new-psdrive -name desktop -psprovider filesystem -root C:\users\student\desktop
get-childitem

new-psdrive -name HKLM-run -psprofider registry -root HKLM:\software\microsoft\windows\currentversion\run

[string]$webDAVShare = '\\live.sysinternals.com\tools'
new-psdrive -name S -PSProvider filesystem -root $WebDAVShare 

```

## PERSISTANCE
```

HKLM\Software\Microsoft\Windows\CurrentVersion\Run

HKU\<SID>\Software\Microsoft\Windows\CurrentVersion\Run

HKLM\SYSTEM\CurrentControlSet\services

HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Folders
cd
HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\User Shell Folders

HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon

```

## REG
```

HKLM\BCD00000000
Replacement of old boot.ini file

HKLM\SAM\SAM
Use "psexec -s -i regedit" from administrator cmd.exe to view the SAM

HKU\<SID>\Software\Policies\Microsoft\Windows\System\Scripts
Group policy Logon/Logoff Scripts defined here

```

## 
```



```

## Alternate Data Streams
```

echo "What time is chow SSGT" > soon.txt
get-childitem .\soon.txt
set-content .\soon.txt -value "chow should be four hours long" -stream secret.info
get-content .\soon.txt

echo "fkvhewlvge;fvbkeqj" > newfile.txt
get-content .\newfile.txt -stream *
get-content .\soon.txt -stream *
get-content .\soon.txt -stream secret.info



```

## 
```



```

## 
```



```

## 
```



```

## 
```



```

## 
```



```

## 
```



```

## 
```



```

## 
```



```

