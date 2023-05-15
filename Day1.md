## Review
```powershell

(get-process notepd*).kill() -- kills notepad process

```

## Cim Classes
```

get-cimclasses
get-ciminstance -classname win32_logicaldisk -filter "drivetype=3" | get-member

gwmi -class win32Logicaldisk -filter "drivetype=3"

```

## Get-ExecutionPolicy
```

set-executionpolicy -ExecutionPolicy Restricted -Scope CurrentUser


```

## Powershell Profiles
```

All Users, All Hosts        $PsHome\Profile.ps1
All Users, Current Host     $PsHome\Microsoft.PowerShell_profile.ps1
Current User, All Hosts     $Home\[My]Documents\Profile.ps1
Current User, Current Host  $Home\[My ]Documents\WindowsPowerShell\Profile.ps1


$PROFILE
persistant changes

*** new-item -itemtype file -path $profile -force ***

Test-Path -Path $profile.currentUsercurrentHost
Test-Path -Path $profile.currentUserAllHosts
Test-Path -Path $profile.AllUsersAllHosts
Test-Path -Path $profile.AllUserscurrentHost

Set Aliases/Variables (Trusted IP's) in Profiles

it reads file everytime powershell is opened



```

## Keylogger for powershell
```

start-transcript C:\commands.txt

```

## trusted hosts
```

get-item WSMan:\localhost\client\trustedhosts

set-item WSMan:\localhost\client\trustedhosts -value 10.1.0.3

get-item WSMan:\localhost\client\trustedhosts



```

## PS Remoting
```

$session = New-PSSession -computername 10.1.0.3 -credentials student
enter-pssession $session

Invoke-command -computername file-server,domain-controller {get-service} -asjob==(background)
Recieve-job <job #>

```

## downloads
```

$url = "longassurl"
$output = "PSScriptroot\bunch of bs"
$wc = new-object system.net.webclient
$wc.downloadfile($url, $output)
(new-object system.net.webclient).downloadfile($url, $output)

```

# Stack #4
```

10.50.36.106 - admin station?
andy.dwyer : BurtMacklinFBI

start2347 start85678

xfreerdp /v:10.50.25.78 /u:student +glyph-cache +clipboard +dynamic-resolution


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

