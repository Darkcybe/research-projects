# ShimCache

The Shimcache (also known as AppCompatCache) allows applications to call properties from earlier Windows versions, avoiding the need to rewrite an application when the host operating system is upgraded. When an application launches, it checks for compatibility and creates a Shimcache item that maintains the executable's last modification date, file path, and file size.

| Windows | XP | 7 | 8 | 10 | 11 |
|---------|----|---|---|----|----|
|         |✅|✅|✅|✅|✅|

| Server | 2003R2 | 2008R2 | 2012R2 | 2016 | 2019 | 2022 |
|--------|--------|--------|--------|------|------|------|
|        |     ✅   |  ✅      |     ✅   |    ✅  |   ✅   |  ✅    |

### Location
```plaintext
# WINDOWS: XP
HKLM\SYSTEM\CurrentControlSet\Control\SessionManager\AppCompatability

# WINDOWS: 7+
HKLM\SYSTEM\CurrentControlSet\Control\Session Manager\AppCompatCache
```

### Interpretation and Investigative Notes

This key contains any executable that runs on the Windows system. This key can be used to determine which computers malware or other applications of interest was executed on. Furthermore, depending on the interpretation of time-based data, you may be able to ascertain the last time the system was executed or that activity occurred.
- Windows XP has a maximum of 96 entries, with the `LastUpdateTime` field being changed when the executable is run.
- Windows 7 and later systems have a maximum of 1024 entries., However the `LastUpdateTime` field does not exist.

The registry key itself is not displayed in an easy to read format if utilizing the native `regedit.exe` tool, therefore parsing with a third party tool is a requirement to analyze the data.

> Entries do not always indicate execution as they may be shimmed prior to execution when first dropped on disk. Execution should be be proven via multiple methods where able.
{: .prompt-info }

## Testing

### Windows 10
- Present

### Windows 11
- Present

## Server 2016
- Present

### Server 2019
- Present

### Server 2022
- Present