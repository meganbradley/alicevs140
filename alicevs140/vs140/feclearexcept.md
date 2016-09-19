---
title: "feclearexcept"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - cpp
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - feclearexcept
apilocation: 
  - api-ms-win-crt-runtime-l1-1-0.dll
  - msvcrt.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: ef419da3-c248-4432-b53c-8e7a475d9533
caps.latest.revision: 7
translation.priority.mt: 
  - de-de
  - ja-jp
---
# feclearexcept
Attempts to clear the floating-point exception flags        specified by the argument.  
  
## Syntax  
  
```  
int feclearexcept(  
   int excepts  
);  
```  
  
#### Parameters  
 `excepts`  
 The exception status flags to clear.  
  
## Return Value  
 Returns zero if `excepts` is zero, or if all        the specified exceptions were successfully cleared. Otherwise, returns a nonzero value.  
  
## Remarks  
 The `feclearexcept` function attempts to clear the floating point exception status flags specified by `excepts`. The function supports these exception macros, defined in fenv.h:  
  
|Exception Macro|Description|  
|---------------------|-----------------|  
|FE_DIVBYZERO|A singularity or pole error occurred in an earlier floating-point operation; an infinity value was created.|  
|FE_INEXACT|The function was forced to round the stored result of an earlier floating-point operation.|  
|FE_INVALID|A domain error occurred in an earlier floating-point operation.|  
|FE_OVERFLOW|A range error occurred; an earlier floating-point operation result was too large to be represented.|  
|FE_UNDERFLOW|An earlier floating-point operation result was too small to be represented at full precision; a denormal value was created.|  
|FE_ALLEXCEPT|The bitwise OR of all supported floating-point exceptions.|  
  
 The `excepts` argument may be zero, or the bitwise OR of one or more of the supported exception macros. The result of any other argument value is undefined.  
  
## Requirements  
  
|Function|C header|C++ header|  
|--------------|--------------|------------------|  
|`feclearexcept`|<fenv.h>|<cfenv\>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [fetestexcept](../vs140/fetestexcept.md)