# Jump Lists
The Windows task bar (Jump List) is engineered to allow users to “jump” or access items they have frequently or recently used quickly and easily. This can include files, applications, and directories to name the major items of significance for forensic investigations.

The data stored in the AutomaticDestinations folder will each have a unique file prepended with the AppID of the associated application, such as the following example which depicts the AppID of Windows Explorer 8.1: `f01b4d95cf55d32a.automaticDestinations-ms`.

WIN: 7+
SRV: 2012

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