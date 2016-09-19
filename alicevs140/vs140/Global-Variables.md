---
title: "Global Variables"
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
ms.assetid: 01d1551c-2f0c-4f72-935c-6442caccf84f
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Global Variables
The Microsoft C run-time library provides the following global variables or macros. Several of these global variables or macros have been deprecated in favor of more-secure functional versions, which we recommend you use instead of the global variables.  
  
|Variable|Description|  
|--------------|-----------------|  
|[__argc, \__argv, \__wargv](../vs140/__argc--__argv--__wargv.md)|Contains the command-line arguments.|  
|[_daylight, _dstbias, _timezone, and _tzname](../vs140/_daylight--_dstbias--_timezone--and-_tzname.md)|Deprecated. Instead, use `_get_daylight`, `_get_dstbias`, `_get_timezone`, and `_get_tzname`.<br /><br /> Adjusts for local time; used in some date and time functions.|  
|[errno, _doserrno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md)|Deprecated. Instead, use `_get_errno`, `_set_errno`, `_get_doserrno`, `_set_doserrno`, `perror` and `strerror`.<br /><br /> Stores error codes and related information.|  
|[_environ, _wenviron](../vs140/_environ--_wenviron.md)|Deprecated. Instead, use `getenv_s`, `_wgetenv_s`, `_dupenv_s`, `_wdupenv_s`, `_putenv_s`, and `_wputenv_s`.<br /><br /> Pointers to arrays of pointers to the process environment strings; initialized at startup.|  
|[_fmode](../vs140/_fmode.md)|Deprecated. Instead, use `_get_fmode` or `_set_fmode`.<br /><br /> Sets default file-translation mode.|  
|[_iob](../vs140/_iob.md)|Array of I/O control structures for the console, files, and devices.|  
|[_pctype, _pwctype, _wctype, _mbctype, _mbcasemap](../vs140/_pctype--_pwctype--_wctype--_mbctype--_mbcasemap.md)|Contains information used by the character-classification functions.|  
|[_pgmptr, _wpgmptr](../vs140/_pgmptr--_wpgmptr.md)|Deprecated. Instead, use `_get_pgmptr` or `_get_wpgmptr`.<br /><br /> Initialized at program startup to the fully-qualified or relative path of the program, the full program name, or the program name without its file name extension, depending on how the program was invoked.|  
  
## See Also  
 [C Run-Time Library Reference](../vs140/C-Run-Time-Library-Reference.md)   
 [Global Constants](../vs140/Global-Constants.md)   
 [__argc, \__argv, \__wargv](../vs140/__argc--__argv--__wargv.md)   
 [_get_daylight](../vs140/_get_daylight.md)   
 [_get_dstbias](../vs140/_get_dstbias.md)   
 [_get_timezone](../vs140/_get_timezone.md)   
 [_get_tzname](../vs140/_get_tzname.md)   
 [perror](../vs140/perror--_wperror.md)   
 [strerror](../vs140/strerror--_strerror--_wcserror--__wcserror.md)   
 [_get_doserrno](../vs140/_get_doserrno.md)   
 [_set_doserrno](../vs140/_set_doserrno.md)   
 [_get_errno](../vs140/_get_errno.md)   
 [_set_errno](../vs140/_set_errno.md)   
 [_dupenv_s, _wdupenv_s](../vs140/_dupenv_s--_wdupenv_s.md)   
 [getenv, _wgetenv](../vs140/getenv--_wgetenv.md)   
 [getenv_s, _wgetenv_s](../vs140/getenv_s--_wgetenv_s.md)   
 [_putenv, _wputenv](../vs140/_putenv--_wputenv.md)   
 [putenv_s, _wputenv_s](../vs140/_putenv_s--_wputenv_s.md)   
 [_get_fmode](../vs140/_get_fmode.md)   
 [_set_fmode](../vs140/_set_fmode.md)