# AmCache

## Location
C:\Windows\AppCompat\Programs\Amcache.hve

WIN: 7+
SRV: 2008 R2+

Tools
AmCache Parser
Get-ForensicAmcache
Registry Explorer (RECmd)
RECmd - Registry Plugins
Sources
Andrea Fortuna - AmCache and Shimcache in Forensic Analysis

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


### Windows Server 2022
Amcache_DeviceContainers.csv
Amcache_DevicePnps.csv
Amcache_DriveBinaries.csv
Amcache_DriverPackages.csv
Amcache_ShortCuts.csv
Amcache_UnassociatedFileEntries.csv

### Windows Server 2019
