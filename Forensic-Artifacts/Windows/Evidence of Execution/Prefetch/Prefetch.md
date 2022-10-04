# Prefetch
Increases performance of a system by pre-loading code pages of commonly used applications. Cache Manager monitors all files and directories referenced for each application or process and maps them into a .pf file. Utilized to know an application was executed on a system.
- Limited to 128 files on XP and Windows 7
- Limited to 1024 files on Windows 8
- `<EXE_NAME>-<HASH>.pf`

| Windows    | XP     | 7      | 8      | 10   | 11   |      |
|------------|--------|--------|--------|------|------|------|
|            | ✅     | ✅    | ✅     | ✅  | ✅   |      |
| **Server** | 2003R2 | 2008R2 | 2012R2 | 2016 | 2019 | 2022 |
|            | ✅*     | ✅*    | ✅*    | ✅*  | ✅*  |       |

> "*" Although prefetch is available on Windows Servers, it is disabled by default. To enable Prefetch on Windows Servers (I was unable to get this working on Windows Server 2022), the following steps can be taken. However, keep in mind that it will need to be enable prior to any nefarious activities occurring and will not provide retrospective artifacts. Prefetch can also be disabled by default when the system detected an SSD being used, enabling can be configured by the same.
> 1. Update or create the `EnablePrefetcher` registry key in `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management\PrefetchParameters`
> 2. Set the `EnablePrefetcher` key value: `0` = Disabled, `1` = Application launch prefetching enabled, `2` = Boot prefetching enabled, `2` = Application launch and boot prefetching enabled.

### Location
```plaintext
C:\Windows\Prefetch
```

### Interpretation and Investigative Notes
- Each Prefetch file will include last time of execution, number of times run, and device and file handles used by the program.
- Date/Time file by that name and path was first executed
  - Creation Date of .pf file (-10 seconds)
- Date/Time file by that name and path was last executed
  - Windows 8+ will contain last 8 times of execution.

## Testing

### Windows 11
- **Interesting Fields**
  - **SourceCreated** = .pf Creation Timestamp
  - **SourceModified** = .pf Modification Timestamp
  - **SourceAccessed** = .pf Last Access Timestamp (Will be overwritten by tooling)
  - **ExecutableName** = Name of executable
  - **RunCount** = Amount of times executed
  - **LastRun** = Timestamp of last execution
  - **PreviousRun#** = Timestamps of previous executions

### Server 2022
- Creating and amending the `EnablePrefetcher` or `EnableSuperfetch` did not enable the service. Attempted to stop SysMain via `sc stop sysmain`, make the registry changes and start SysMain again, and performed reboots to no avail.

# Sources
- [Microsoft - Disabling Prefetch](https://learn.microsoft.com/en-us/previous-versions/windows/embedded/ms940847(v=winembedded.5)?redirectedfrom=MSDN)