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

