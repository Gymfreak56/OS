# Forensics
## Memory Analysis
```



```

## Order of Volitility
```

CPU registers, cache

Routing table, ARP cache, process table, kernel stats, memory

Temporary file systems

Disk

Remote logging and monitoring data

Physical configuration, network topology

Archival media - backups

```

## Pmem (Persistence memory)
```

Linpmem
Winpmem
OSXpmem

```

## Volitility
```

Tool used for memory analysis

```

##
```

CASE SENSITIVE
.exe -f <file> --profile=<profile> <what you want to do>
.exe -f <file> imageinfo
.exe -f <file> --profile=<profile> -h ---- help

```

## volitility
```

psscan
pslist
pstree

procdump -p 1640 -D . -- carve out executable
get-filehash -- compare with known viruses(VirusTotal)

STRINGS ANALYSIS
memdump -p 1640 -D . -- Strings Analysis
strings.exe -accepteula <file> > <file>
search for ip addresses

connections
connscan

```

## Recomended commands
```

Identify Rogue Processes: slist vs. psscan; output results to a dot file to have a nice visual representation of parent/child process relationships

Process validity - look for things that are off (misspellings, high PIDs, multiples that shouldn’t be, etc.)

DLLs and Handles: dlllist, dlldump

Network Artifacts: connections

Hunt for Code Injection: malfind

Check for rootkit: psscan, devicetree

Dump suspicious processes and drivers: dlldump, procdump, memdump, filescan, svcscan, driverirp

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
