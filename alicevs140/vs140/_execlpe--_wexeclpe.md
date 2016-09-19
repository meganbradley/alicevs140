---
title: "_execlpe, _wexeclpe"
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
  - _execlpe
  - _wexeclpe
apilocation: 
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 07b861da-3e7e-4f1d-bb80-ad69b55e5162
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _execlpe, _wexeclpe
Loads and executes new child processes.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
intptr_t _execlpe(   
   const char *cmdname,  
   const char *arg0,  
   ... const char *argn,  
   NULL,  
   const char *const *envp   
);  
intptr_t _wexeclpe(   
   const wchar_t *cmdname,  
   const wchar_t *arg0,  
   ... const wchar_t *argn,  
   NULL,  
   const wchar_t *const *envp   
);  
```  
  
#### Parameters  
 `cmdname`  
 Path of the file to execute.  
  
 `arg0`, `...``argn`  
 List of pointers to parameters.  
  
 `envp`  
 Array of pointers to environment settings.  
  
## Return Value  
 If successful, these functions do not return to the calling process. A return value of –1 indicates an error, in which case the `errno` global variable is set.  
  
|`errno` value|Description|  
|-------------------|-----------------|  
|`E2BIG`|The space required for the arguments and environment settings exceeds 32 KB.|  
|`EACCES`|The specified file has a locking or sharing violation.|  
|`EINVAL`|Invalid parameter.|  
|`EMFILE`|Too many files open (the specified file must be opened to determine whether it is executable).|  
|`ENOENT`|The file or path not found.|  
|`ENOEXEC`|The specified file is not executable or has an invalid executable-file format.|  
|`ENOMEM`|Not enough memory is available to execute the new process; the available memory has been corrupted; or an invalid block exists, indicating that the calling process was not allocated properly.|  
  
 For more information about these and other return codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 Each of these functions loads and executes a new process, passing each command-line argument as a separate parameter and also passing an array of pointers to environment settings. These functions use the `PATH` environment variable to find the file to execute.  
  
 The `_execlpe` functions validate their parameters. If either `cmdname` or `arg0` is a null pointers or empty string, these functions invoke the invalid parameter handler as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions set `errno` to `EINVAL` and return -1. No new process is launched.  
  
## Requirements  
  
|Function|Required header|Optional header|  
|--------------|---------------------|---------------------|  
|`_execlpe`|<process.h>|<errno.h>|  
|`_wexeclpe`|<process.h> or <wchar.h>|<errno.h>|  
  
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