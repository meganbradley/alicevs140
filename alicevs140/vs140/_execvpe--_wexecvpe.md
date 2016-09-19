---
title: "_execvpe, _wexecvpe"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - _execvpe
  - _wexecvpe
apilocation: 
  - msvcr90.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: c0c3c986-d9c0-4814-a96c-10f0b3092766
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _execvpe, _wexecvpe
Loads and runs new child processes.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
intptr_t _execvpe(   
   const char *cmdname,  
   const char *const *argv,  
   const char *const *envp   
);  
intptr_t _wexecvpe(   
   const wchar_t *cmdname,  
   const wchar_t *const *argv,  
   const wchar_t *const *envp   
);  
```  
  
#### Parameters  
 `cmdname`  
 Path of the file to execute.  
  
 `argv`  
 Array of pointers to parameters.  
  
 `envp`  
 Array of pointers to environment settings.  
  
## Return Value  
 If successful, these functions do not return to the calling process. A return value of –1 indicates an error, in which case the `errno` global variable is set.  
  
|`errno` value|Description|  
|-------------------|-----------------|  
|`E2BIG`|The space that's required for the arguments and environment settings exceeds 32 KB.|  
|`EACCES`|The specified file has a locking or sharing violation.|  
|`EMFILE`|Too many files are open. (The specified file must be opened to determine whether it is executable.)|  
|`ENOENT`|The file or path is not found.|  
|`ENOEXEC`|The specified file is not executable or has an invalid executable-file format.|  
|`ENOMEM`|Not enough memory is available to execute the new process; the available memory has been corrupted; or an invalid block exists, which indicates that the calling process was not allocated correctly.|  
  
 For more information about these and other return codes, see [errno, _doserrno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 Each of these functions loads and executes a new process, and passes an array of pointers to command-line arguments and an array of pointers to environment settings. These functions use the `PATH` environment variable to find the file to execute.  
  
 The `_execvpe` functions validate their parameters. If the `cmdname` is a null pointer, or if `argv` is a null pointer, a pointer to an empty array, or a pointer to an array that contains an empty string as the first argument, these functions invoke the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions set `errno` to `EINVAL` and return -1. No process is launched.  
  
## Requirements  
  
|Function|Required header|Optional header|  
|--------------|---------------------|---------------------|  
|`_execvpe`|<process.h>|<errno.h>|  
|`_wexecvpe`|<process.h> or <wchar.h>|<errno.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
 See the example in [_exec, _wexec Functions](../vs140/_exec--_wexec-Functions.md).  
  
## .NET Framework Equivalent  
  
-   [System::Diagnostics::Process Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.process.aspx)  
  
-   [System::Diagnostics::ProcessStartInfo Class](https://msdn.microsoft.com/en-us/library/system.diagnostics.processstartinfo.aspx)  
  
## See Also  
 [Process and Environment Control](../vs140/Process-and-Environment-Control.md)   
 [_exec, _wexec Functions](../vs140/_exec--_wexec-Functions.md)   
 [abort](../vs140/abort.md)   
 [atexit](../vs140/atexit.md)   
 [exit, _Exit, _exit](../vs140/exit--_Exit--_exit.md)   
 [_onexit, _onexit_m](../vs140/_onexit--_onexit_m.md)   
 [_spawn, _wspawn Functions](../vs140/_spawn--_wspawn-Functions.md)   
 [system, _wsystem](../vs140/system--_wsystem.md)