---
title: "log1p, log1pf, log1pl"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - cpp
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - log1p
  - log1pf
  - log1pl
apilocation: 
  - msvcrt.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - api-ms-win-crt-math-l1-1-0.dll
apitype: DLLExport
ms.assetid: a40d965d-b4f6-42f4-ba27-2395546f7c12
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# log1p, log1pf, log1pl
Computes the natural logarithm of 1 plus the specified value.  
  
## Syntax  
  
```  
double log1p(  
   double x  
);  
  
float log1p(  
   float x  
); //C++ only  
  
long double log1p(  
   long double x  
); //C++ only  
  
float log1pf(  
   float x  
);  
  
long double log1pl(  
   long double x  
);  
  
```  
  
#### Parameters  
 `x`  
 The floating-point argument.  
  
## Return Value  
 If successful, returns the natural (base-e) log of (`x`+1).  
  
 Otherwise, may return one of the following values:  
  
|Input|Result|SEH exception|errno|  
|-----------|------------|-------------------|-----------|  
|+inf|+inf|||  
|Denormals|Same as input|UNDERFLOW||  
|±0|Same as input|||  
|-1|-inf|DIVBYZERO|ERANGE|  
|< -1|nan|INVALID|EDOM|  
|-inf|nan|INVALID|EDOM|  
|±SNaN|Same as input|INVALID||  
|±QNaN, indefinite|Same as input|||  
  
 The `errno` value is set to ERANGE if `x` = -1. The `errno` value is set to EDOM if `x` < −1.  
  
## Remarks  
 The `log1p` functions may be more accurate than using log(`x`+1) when x is near 0.  
  
 Because C++ allows overloading, you can call overloads of `log1p` that take and return float and long double types. In a C program, `log1p` always takes and returns a double.  
  
 If `x` is a natural number, this function returns the logarithm of the factorial of (`x`-1).  
  
## Requirements  
  
|Function|C header|C++ header|  
|--------------|--------------|------------------|  
|`log1p`,                `log1pf`,  `log1pl`|<math.h>|<cmath\>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [log2, log2f, log2l](../vs140/log2--log2f--log2l.md)   
 [log, logf, log10, log10f](../vs140/log--logf--log10--log10f.md)