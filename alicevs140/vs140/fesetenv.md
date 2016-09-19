---
title: "fesetenv"
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
  - fesetenv
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
ms.assetid: ffc64fff-8ea7-4d59-9e04-ff96ef8cd012
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# fesetenv
Sets the current floating-point environment.  
  
## Syntax  
  
```  
int fesetenv(  
   const fenv_t *penv  
);  
  
```  
  
#### Parameters  
 `penv`  
 Pointer to a `fenv_t` object that contains a floating-point environment as set by a call to [fegetenv](assetId:///61df848d-6ba8-4c6e-be35-216436fe7736) or [feholdexcept](assetId:///c286ace3-ec39-482a-be8b-f998d31003d9). You can also specify the default startup floating-point environment by using the FE_DFL_ENV macro.  
  
## Return Value  
 Returns 0 if the environment was successfully set.        Otherwise, returns a nonzero value.  
  
## Remarks  
 The `fesetenv` function sets the current floating-point environment from the value stored in the `fenv_t` object pointed to by `penv`. The floating point environment is the set of status flags and control modes that affect floating-point calculations. This includes the rounding mode and the status flags for floating-point exceptions.  If `penv` is not FE_DFL_ENV or does not point to a valid `fenv_t` object, subsequent behavior is undefined.  
  
 A call to this function sets the exception status flags that are in the `penv` object, but it does not raise those exceptions.  
  
 To use this function, you must turn off floating-point optimizations that could prevent access by using the `#pragma fenv_access(on)` directive prior to the call. For more information, see [fenv_access](../vs140/fenv_access.md).  
  
## Requirements  
  
|Function|C header|C++ header|  
|--------------|--------------|------------------|  
|`fesetenv`|<fenv.h>|<cfenv\>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [fegetenv](../vs140/fegetenv.md)   
 [feclearexcept](../vs140/feclearexcept.md)   
 [feholdexcept](../vs140/feholdexcept.md)   
 [fesetexceptflag](../vs140/fesetexceptflag.md)