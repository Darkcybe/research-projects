# Windows Timeline (Activities Cache.db)
Windows 10 records recently used applications and files in a “timeline” accessible via the “WIN+TAB” key. The data is recorded in a SQLite database. Windows 11 removed the “WIN+TAB” functionality, however the ActivitiesCache.db still remains.

WIN: 10+
SRV: NULL

# Location
C:\Users\%PROFILE%\AppData\Local\ConnectedDevicesPlatform\L.%PROFILE%\ActivitiesCache.db

# Interpretation and Investigative Notes
Tracks application execution and provides a focus count per application.

# Sources
Kacos2000 - Windows Timeline
Microsoft - Windows Activity History and Your Privacy

# Testing

## Windows 11
C:\Users\%PROFILE%\AppData\Local\ConnectedDevicesPlatform\L.%PROFILE%\ActivitiesCache.db

ActivitiesCache.db
ActivitiesCache.db-shm
ActivitiesCache.db-wal

## Windows 10

## Windows Server 2022
C:\Users\%PROFILE%\AppData\Local\ConnectedDevicesPlatform\L.%PROFILE%\ActivitiesCache.db

ActivitiesCache.db
ActivitiesCache.db-shm
ActivitiesCache.db-wal

## Windows Server 2019
