# LastVisitedMRU
The LastVisitedMRU is responsible for tracking specific executables used by an application to open files documented under the OpenSaveMRU registry key. In addition, each value tracks the directory location for the last file that was accessed by that application. The information can provide forensic insight into an applications execution and file and folder interaction.

**WIN:** XP+ <br>
**SRV:** 2003+

# Location
```plaintext
# WINDOWS: XP
NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\ComDlg32\LastVisitedMRU
# WINDOWS: 7+
NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\ComDlg32\LastVisitedPidlMRU
```

## Interpretation and Investigative Notes
Tracks the application executables used to open files in OpenSaveMRU and the last file path used, for example: Notepad.exe was last run under the `C:\%USERPROFILE%\Desktop` directory.

## Testing

### Windows 11
NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\ComDlg32\LastVisitedPidlMRU

Interesting Fields
- Executable: Records the parent application
- Absolute Path: Records the file opened
- Opened On: Date-time-group of last access time

### Server 2022
NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\ComDlg32\LastVisitedPidlMRU

Interesting Fields
- Executable: Records the parent application
- Absolute Path: Records the file opened
- Opened On: Date-time-group of last access time