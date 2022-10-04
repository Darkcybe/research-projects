# RecentApps
GUI Program execution launched on the Windows 10 System is tracked in the RecentApps key.

| Windows | XP | 7 | 8 | 10 | 11 |
|---------|----|---|---|----|----|
|         |    |   |   | ✅ |    |

| Server | 2003R2 | 2008R2 | 2012R2 | 2016 | 2019 | 2022 |
|--------|--------|--------|--------|------|------|------|
|        |        |        |        |      |      |      |

**WIN:** 10 <br>
**SRV:** NULL

### Location
```plaintext
NTUSER.DAT\Software\Microsoft\Windows\Current Version\Search\RecentApps
```

### Interpretation and Investigative Notes
- Each GUID key points to a recent application.
  - `AppID` = Name of Application
  - `LastAccessTime` = Last execution time in UTC
  - `LaunchCount` = Number of times executed

## Testing

### Windows 10
- Only Microsoft Windows 10 versions V1607-1709 appear to populate the RecentApps registry key.

### Windows 11
- 

### Server 2019
-

### Server 2022
- 

# Sources
- 