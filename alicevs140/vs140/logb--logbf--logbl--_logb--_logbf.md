---
title: "logb, logbf, logbl, _logb, _logbf"
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
  - logb
  - _logb
  - _logbl
  - logbf
  - logbl
apilocation: 
  - msvcr90.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 780c4daa-6fe6-4fbc-9412-4c1ba1a1766f
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# logb, logbf, logbl, _logb, _logbf
Extracts the exponent value of a floating-point argument.  
  
## Syntax  
  
```  
double logb(  
   double x   
);  
float logb(  
   float x   
); // C++ only  
long double logb(  
   long double x   
); // C++ only   
float logbf(  
   float x   
);  
long double logbl(  
   long double x   
);  
double _logb(  
   double x   
);  
float _logbf(  
   float x   
);  
```  
  
#### Parameters  
 x  
 A floating-point value.  
  
## Return Value  
 `logb` returns the unbiased exponent value of `x` as a signed integer represented as a floating-point value.  
  
## Remarks  
 The `logb` functions extract the exponential value of the floating-point argument `x`, as though `x` were represented with infinite range. If the argument `x` is denormalized, it is treated as if it were normalized.  
  
 Because C++ allows overloading, you can call overloads of `logb` that take and return `float` or `long double` values. In a C program, `logb` always takes and returns a `double`.  
  
|Input|SEH exception|Matherr exception|  
|-----------|-------------------|-----------------------|  
|± QNAN,IND|None|_DOMAIN|  
|± 0|ZERODIVIDE|_SING|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_logb`|<float.h>|  
|`logb`, `logbf`, `logbl`, `_logbf`|<math.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [frexp](../vs140/frexp.md)