---
title: "_get_doserrno"
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
  - _get_doserrno
apilocation: 
  - msvcr80.dll
  - msvcr110.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 7fec7be3-6e39-4181-846b-8ef24489361c
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _get_doserrno
Gets the error value returned by the operating system before it is translated into an `errno` value.  
  
## Syntax  
  
```  
errno_t _get_doserrno(   
   int * pValue   
);   
```  
  
#### Parameters  
 [out] `pValue`  
 A pointer to an integer to be filled with the current value of the `_doserrno` global macro.  
  
## Return Value  
 If `_get_doserrno` succeeds, it returns zero; if it fails, it returns an error code. If `pValue` is `NULL`, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, this function sets `errno` to `EINVAL` and returns `EINVAL`.  
  
## Remarks  
 The `_doserrno` global macro is set to zero during CRT initialization, before process execution begins. It is set to the operating-system error value returned by any system-level function call that returns an operating-system error, and it is never reset to zero during execution. When you write code to check the error value returned by a function, always clear `_doserrno` by using [_set_doserrno](../vs140/_set_doserrno.md) before the function call. Because another function call may overwrite `_doserrno`, check the value by using `_get_doserrno` immediately after the function call.  
  
 We recommend [_get_errno](../vs140/_get_errno.md) instead of `_get_doserrno` for portable error codes.  
  
 Possible values of `_doserrno` are defined in <errno.h>.  
  
## Requirements  
  
|Routine|Required header|Optional header|  
|-------------|---------------------|---------------------|  
|`_get_doserrno`|<stdlib.h>, <cstdlib\> (C++)|<errno.h>, <cerrno\> (C++)|  
  
 `_get_doserrno` is a Microsoft extension. For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## See Also  
 [_set_doserrno](../vs140/_set_doserrno.md)   
 [doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md)