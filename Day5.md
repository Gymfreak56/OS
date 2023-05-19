## Boot Process
```

Big Mike Got Killed In Russia 

BIOS
MBR
GRUB
KERNEL
INIT
RUNLEVEL

```

## BIOS
```

Preforms POST
reads and executes first sector of MBR load bootloader to memory


```

## DMI (Desktop Management Interface)
```

dmidecode -t x - bios

```

## Master Boot Record 
```

MBR - bootstrap loader for bootloader, partition table, and magic number
4 Partitions
512 bytes

Magic Number ***55aa***

how to copy MBR

***dd if=/dev/vda of=MBRcopy bs=512 count=1***

```

## List block devices
```

lsblk
16 bytes in a partition

```

## GPT (GUID Partition Table)
```

not backwards compatible
MBR = 2TB
GPT = 9ZB

```

## GRUB
```

/boot/grub/menu.lst
Selects Kernel



MBR:
Stage 1 : boot.img located in the first 440 bytes of the MBR loads…

Stage 1.5 : core.img located in the MBR between the bootstrap and first partition. It loads…

Stage 2 : /boot/grub/i386-pc/normal.mod which loads the grub menu and then reads

              /boot/grub/grub.cfg Which displays a list of Linux kernels available to load on the system

CPT:
grubx64.efi Located on an EFI partition or in /boot loads…

/boot/grub/x86_64-efi/normal.mod

/boot/grub/grub.cfg Which displays a list of Linux kernels available to load on the system

```

## Kernel
```

uncompress itself into RAM
Detects CPU type, establishes memory management, establishes page tables
mounts the root of the file system
executes /sbin/

sudo strace cat /etc/passwd

lsmod - list modules



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

