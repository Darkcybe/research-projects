# BAM and DAM
Windows BAM and DAM are updated when Windows boots and controls the activity of background applications and is found on all Windows devices and is managed by `C:\Windows\System32\drivers\bam.sys`. DAM is only populated with details of applications on Windows Tablets and Mobile devices although the empty registry key will be present on host devices.

BAM and DAM entries are only stored during a session, with events clearing upon reboot or when entries have been present in the key for over 7 days. Another item to consider is that executables hosted on removable media are not recorded in the BAM or DAM.

| Windows    | XP     | 7      | 8      | 10   | 11   |      |
|------------|--------|--------|--------|------|------|------|
|            |       |       |       | ✅    | ✅    |      |
| **Server** | 2003R2 | 2008R2 | 2012R2 | 2016 | 2019 | 2022 |
|            |       |       |       |     | ✅    | ✅    |

## Location
HKLM\System\CurrentControlSet\Services\bam\state\UserSettings\{SID}

> `CurrentControlSet` may be substituted by `ControlSet001` or `ControlSet002`. The `ControlSet00x` are alternating backups of the `CurrentControlSet`.

## Testing

### Windows 11
SYSTEM\CurrentControlSet\Services\bam\state\UserSettings\{SID}
Columns
- Program (full filepath)
- Execution Time

### Server 2022
SYSTEM\CurrentControlSet\Services\bam\state\UserSettings\{SID}
Columns
- Program (full filepath)
- Execution Time

### Server 2019
SYSTEM\CurrentControlSet\Services\bam\state\UserSettings\{SID}
Columns
- Program (full filepath)
- Execution Time

### Server 2016
Does not exist