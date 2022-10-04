# AmCache

| Windows    | XP     | 7      | 8      | 10   | 11   |      |
|------------|--------|--------|--------|------|------|------|
|            |       | ✅      | ✅      | ✅    | ✅    |      |
| **Server** | 2003R2 | 2008R2 | 2012R2 | 2016 | 2019 | 2022 |
|            |       | ✅      | ✅      | ✅    | ✅    | ✅    |

## Location
```powershell
C:\Windows\AppCompat\Programs\Amcache.hve
```

## Testing
Amcache.hve locked by system when attempting to locally copy. Running Registry Explorer as an Administrator allows the hive to be loaded and navigated through as well as the option to output to .csv. AmcacheParser can also be run as an Administrator on the live hive which dumps .csv output

### Windows 11
#### AmcacheParser
Amcache_DeviceContainers.csv
Amcache_DevicePnps.csv
Amcache_DriveBinaries.csv
Amcache_DriverPackages.csv
Amcache_ShortCuts.csv
Amcache_UnassociatedFileEntries.csv

### Windows 10
Amcache_DeviceContainers.csv
Amcache_DevicePnps.csv
Amcache_DriveBinaries.csv
Amcache_DriverPackages.csv
Amcache_ShortCuts.csv
Amcache_UnassociatedFileEntries.csv

### Windows Server 2022
Amcache_DeviceContainers.csv
Amcache_DevicePnps.csv
Amcache_DriveBinaries.csv
Amcache_DriverPackages.csv
Amcache_ShortCuts.csv
Amcache_UnassociatedFileEntries.csv

### Windows Server 2019
Amcache_DeviceContainers.csv
Amcache_DevicePnps.csv
Amcache_DriveBinaries.csv
Amcache_DriverPackages.csv
Amcache_ShortCuts.csv
Amcache_UnassociatedFileEntries.csv