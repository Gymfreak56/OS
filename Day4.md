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

##
```



```

##
```



```

