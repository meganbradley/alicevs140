---
title: "_execl, _wexecl"
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
  - _execl
  - _wexecl
apilocation: 
  - msvcr80.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 81fefb8a-0a06-4221-b2bc-be18e38e89f4
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _execl, _wexecl
Loads and executes new child processes.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
intptr_t _execl(   
   const char *cmdname,  
   const char *arg0,  
   ... const char *argn,  
   NULL   
);  
intptr_t _wexecl(  
   const wchar_t *cmdname,  
   const wchar_t *arg0,  
   ... const wchar_t *argn,  
   NULL   
);  
```  
  
#### Parameters  
 `cmdname`  
 Path of the file to be executed.  
  
 `arg0`, `...``argn`  
 List of pointers to the parameters.  
  
## Return Value  
 If successful, these functions do not return to the calling process. A return value of –1 indicates an error, in which case the `errno` global variable is set.  
  
|errno value|Description|  
|-----------------|-----------------|  
|`E2BIG`|The space required for the arguments and environment settings exceeds 32 KB.|  
|`EACCES`|The specified file has a locking or sharing violation.|  
|`EINVAL`|Invalid parameter (one or more of the parameters was a null pointer or empty string).|  
|`EMFILE`|Too many files open (the specified file must be opened to determine whether it is executable).|  
|`ENOENT`|The file or path is not found.|  
|`ENOEXEC`|The specified file is not executable or has an invalid executable-file format.|  
|`ENOMEM`|Not enough memory is available to execute the new process; the available memory has been corrupted; or an invalid block exists, indicating that the calling process was not allocated properly.|  
  
## Remarks  
 Each of these functions loads and executes a new process, passing each command-line argument as a separate parameter. The first argument is the command or executable file name, and the second argument should be the same as the first. It becomes `argv[0]` in the executed process. The third argument is the first argument, `argv[1]`, of the process being executed.  
  
 The `_execl` functions validate their parameters. If either `cmdname` or `arg0` is a null pointer or empty string, these functions invoke the invalid parameter handler as described in [Parameter Validation](../vs140/Parameter-Validation.md) If execution is allowed to continue, these functions set `errno` to `EINVAL` and return -1. No new process is executed.  
  
## Requirements  
  
|Function|Required header|Optional header|  
|--------------|---------------------|---------------------|  
|`_execl`|<process.h>|<errno.h>|  
|`_wexecl`|<process.h> or <wchar.h>|<errno.h>|  
  
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