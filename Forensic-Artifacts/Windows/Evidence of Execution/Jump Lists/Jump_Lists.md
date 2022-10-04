# Jump Lists
The Windows task bar (Jump List) is engineered to allow users to “jump” or access items they have frequently or recently. This can include files, applications, and directories to name the major items of significance for forensic investigations.

The data stored in the AutomaticDestinations directory contains a unique file for each application prepended with a unique Application ID (AppID) correlated to the associated application, such as the following example which depicts the AppID of Windows Explorer 8.1: `f01b4d95cf55d32a.automaticDestinations-ms`.

| Windows    | XP     | 7      | 8      | 10   | 11   |      |
|------------|--------|--------|--------|------|------|------|
|            |        | ✅      | ✅      | ✅    | ✅    |      |
| **Server** | 2003R2 | 2008R2 | 2012R2 | 2016 | 2019 | 2022 |
|            |        |        | ✅      | ✅    | ✅    | ✅    |

## Location
C:%USERPROFILE%\AppData\Roaming\Microsoft\Windows\Recent\AutomaticDestinations

## Testing

### Windows 11
C:%USERPROFILE%\AppData\Roaming\Microsoft\Windows\Recent\AutomaticDestinations
- TargetCreationDate
- TargetModificationDate
- TargetLastAccessedDate
- LocalPath
- Interaction count

### Server 2022
C:%USERPROFILE%\AppData\Roaming\Microsoft\Windows\Recent\AutomaticDestinations
- TargetCreationDate
- TargetModificationDate
- TargetLastAccessedDate
- LocalPath
- Interaction count

### Server 2012
C:%USERPROFILE%\AppData\Roaming\Microsoft\Windows\Recent\AutomaticDestinations
- TargetCreationDate
- TargetModificationDate
- TargetLastAccessedDate
- LocalPath
- Interaction count