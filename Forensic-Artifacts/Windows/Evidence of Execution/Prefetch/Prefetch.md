# Prefetch
Increases performance of a system by pre-loading code pages of commonly used applications. Cache Manager monitors all files and directories referenced for each application or process and maps them into a .pf file. Utilized to know an application was executed on a system.
- Limited to 128 files on XP and Windows 7
- Limited to 1024 files on Windows 8
- `<EXE_NAME>-<HASH>.pf`

| OS Category | Applicability |
| --- | --- |
| Windows XP | :white-check-box: |
| Windows 7 |
| Windows 8 |
| Windows 10 |

| Windows | XP | 7 | 8 | 10 | 11 |
| --- | --- | --- | --- | --- | --- |
| | x | x | | | |
| --- | --- | --- | --- | --- | --- |
| Server | 2003 | 2008R2 | 2012R2 | 2016 | 2019 | 2022 |
| | x | | | | |

**WIN:** XP+ <br>
**SRV:** NULL

### Location
```plaintext
C:\Windows\Prefetch
```

### Interpretation and Investigative Notes
- Each .pf file will include last time of execution, number of times run, and device and file handles used by the program.
- Date/Time file by that name and path was first executed
  - Creation Date of .pf file (-10 seconds)
- Date/Time file by that name and path was last executed
  - Windows 8+ will contain last 8 times of execution.

## Testing

### Windows 11


### Server 2022
