---
title: "expm1, expm1f, expm1l"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - expm1l
  - expm1
  - expm1f
apilocation: 
  - msvcr110.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 2a4dd2d9-370c-42b0-9067-0625efa272e0
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# expm1, expm1f, expm1l
Computes the base-e exponential of a value, minus one.  
  
## Syntax  
  
```  
double expm1(   
   double x   
);  
float expm1(  
   float x  
);  // C++ only  
long double expm1(  
   long double x  
);  // C++ only  
float expm1f(  
   float x  
);  
long double expm1l(  
   long double x  
);  
```  
  
#### Parameters  
 `x`  
 The floating-point exponential value.  
  
## Return Value  
 The `expm1` functions return a floating-point value that represents e<sup>x</sup> – 1, if successful. On overflow, `expm1` returns `HUGE_VAL`, `expm1f` returns `HUGE_VALF`, `expm1l` returns `HUGE_VALL`, and `errno` is set to `ERANGE`. For more information about return codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 Because C++ allows overloading, you can call overloads of `expm1` that take and return `float` and `long double` values. In a C program, `expm1` always takes and returns a `double`.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`expm1`, `expm1f`, `expm1l`|<math.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [exp2, exp2f, exp2l](assetId:///a7974629-be1e-4196-a562-6624a0732003)   
 [pow](../vs140/pow--powf--powl.md)