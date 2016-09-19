---
title: "_putenv_s, _wputenv_s"
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
  - _wputenv_s
  - _putenv_s
apilocation: 
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: fbf51225-a8da-4b9b-9d7c-0b84ef72df18
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _putenv_s, _wputenv_s
Creates, modifies, or removes environment variables. These are versions of [_putenv, _wputenv](../vs140/_putenv--_wputenv.md) but have security enhancements, as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/en-us/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
errno_t _putenv_s(  
   const char *name,  
   const char *value   
);  
errno_t _wputenv_s(  
   const wchar_t *name,  
   const wchar_t *value  
);  
```  
  
#### Parameters  
 `name`  
 The environment variable name.  
  
 `value`  
 The value to set the environment variable to.  
  
## Return Value  
 Returns 0 if successful, or an error code.  
  
### Error Conditions  
  
|`name`|`value`|Return value|  
|------------|-------------|------------------|  
|`NULL`|any|`EINVAL`|  
|any|`NULL`|`EINVAL`|  
  
 If one of the error conditions occurs, these functions invoke an invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions return `EINVAL` and set `errno` to `EINVAL`.  
  
## Remarks  
 The `_putenv_s` function adds new environment variables or modifies the values of existing environment variables. Environment variables define the environment in which a process executes (for example, the default search path for libraries to be linked with a program). `_wputenv_s` is a wide-character version of `_putenv_s`; the `envstring` argument to `_wputenv_s` is a wide-character string.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tputenv_s`|`_putenv_s`|`_putenv_s`|`_wputenv_s`|  
  
 `name` is the name of the environment variable to be added or modified and `value` is the variable's value. If `name` is already part of the environment, its value is replaced by `value`; otherwise, the new `name` variable and its `value` are added to the environment. You can remove a variable from the environment by specifying an empty string (that is, "") for `value`.  
  
 `_putenv_s` and `_wputenv_s` affect only the environment that is local to the current process; you cannot use them to modify the command-level environment. These functions operate only on data structures that are accessible to the run-time library and not on the environment "segment" that the operating system creates for a process. When the current process terminates, the environment reverts to the level of the calling process, which in most cases is the operating-system level. However, the modified environment can be passed to any new processes that are created by `_spawn`, `_exec`, or `system`, and these new processes get any new items that are added by `_putenv_s` and `_wputenv_s`.  
  
 Do not change an environment entry directly; instead, use `_putenv_s` or `_wputenv_s` to change it. In particular, directly freeing elements of the `_environ[]` global array might cause invalid memory to be addressed.  
  
 `getenv` and `_putenv_s` use the global variable `_environ` to access the environment table; `_wgetenv` and `_wputenv_s` use `_wenviron`. `_putenv_s` and `_wputenv_s` may change the value of `_environ` and `_wenviron`, and thereby invalidate the `envp` argument to `main` and the `_wenvp` argument to `wmain`. Therefore, it is safer to use `_environ` or `_wenviron` to access the environment information. For more information about the relationship of `_putenv_s` and `_wputenv_s` to global variables, see [_environ, _wenviron](../vs140/_environ--_wenviron.md).  
  
> [!NOTE]
>  The `_putenv_s` and `_getenv_s` families of functions are not thread-safe. `_getenv_s` could return a string pointer while `_putenv_s` is modifying the string, and thereby cause random failures. Make sure that calls to these functions are synchronized.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_putenv_s`|<stdlib.h>|  
|`_wputenv_s`|<stdlib.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
 For a sample that shows how to use `_putenv_s`, see [getenv_s, _wgetenv_s](../vs140/getenv_s--_wgetenv_s.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Process and Environment Control](../vs140/Process-and-Environment-Control.md)   
 [getenv, _wgetenv](../vs140/getenv--_wgetenv.md)   
 [_searchenv, _wsearchenv](../vs140/_searchenv--_wsearchenv.md)