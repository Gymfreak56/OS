# Windows Boot Process
## BIOS vs. UEFI
```

BIOS
MBR
bootmgr (BCD)
BCD
OS Loader (winload.exe/winresume.exe)

UEFI
GPT
bootmgrfw.efi (BCD)
BCD
OS Loader (winload.efi/winresume.efi) 

```

## Pre Boot Process
```

POST (Power On Self Test)
BIOS                                      UEFI
MBR                                       GUID Partition Table (Table of contents)(Loads OS)
---                                       Volume Boot Sector
NTLDR.exe Bootmgr.exe                     Bootmgrfw.efi
Boot.ini  BCD                             BCD
---       Winload.exe/winresume.exe       winload.efi/winresume.efi
NTOSKRNL  NTOSKRNL                        NTOSKRNL

```

## Boot Process
```

boot.ini -- old
ntldr - old

```

## SMSS.EXE
```

Master Session Manager - Sets environmental varriables, Sets C:\pagefile.sys, Loads WIN32K.SYS for subsystem

CSRSS.EXE
WININIT.EXE
SMSS.EXE - Winlogon.exe

```

## CSRSS.EXE
```

Subsystem components
user mode dlls 
conhost.exe

```

## WININIT
```

Windows initialization Process
Services.exe
LSASS.exe

```

## Services.exe
```

Service Control Manager
starts all services w/ start value of (0x2)

```

## Lsass.exe
```

Local security authority sub system

```

## BCDEDIT
```

Boot Configuration Data

BCD-config - bcdedit.exe
backup bcd - bcdedit /export C:\SAVEDBCD

bcdedit
bcdedit /export C:\BCD.bk -- create backup of important file
bcdedit /import C:\BCD.bk -- 
bcdedit /set {current} description "Windows 7 - Lion Den"
bcdedit /create {ntldr} /d "Windows XP Pro SP2 - Tiger Paw"
bcdedit /set {ntldr} device partition=C:
bcdedit /set {ntldr} path /ntldr
bcdedit /delete {ntldr}

```

## HAL.dll
```

Layer between kernel & hardware
Hardware Abstraction Layer - lets kernel talk to hardware

```

## Cyber KillChain
```

Recon
Weaponization
Delivery
Exploitation
Installation
Command & Controll
Actions On Objective

```

## MITRE Attack Framework
```

Assists in finding what happened next

```

## Services
```

sc query spooler

```

##
```



```

