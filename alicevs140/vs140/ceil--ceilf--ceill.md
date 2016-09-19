---
title: "ceil, ceilf, ceill"
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
  - ceilf
  - ceil
  - ceill
apilocation: 
  - msvcr120.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr100.dll
  - ntdll.dll
  - api-ms-win-crt-math-l1-1-0.dll
apitype: DLLExport
ms.assetid: f4e5acab-5c8f-4b10-9ae2-9561e6453718
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ceil, ceilf, ceill
Calculates the ceiling of a value.  
  
## Syntax  
  
```  
double ceil(   
   double x   
);  
float ceil(  
   float x  
);  // C++ only  
long double ceil(  
   long double x  
);  // C++ only  
float ceilf(  
   float x  
);  
long double ceill(  
   long double x  
);  
```  
  
#### Parameters  
 `x`  
 Floating-point value.  
  
## Return Value  
 The `ceil` functions return a floating-point value that represents the smallest integer that is greater than or equal to `x`. There is no error return.  
  
|Input|SEH Exception|Matherr Exception|  
|-----------|-------------------|-----------------------|  
|± `QNAN`,`IND`|none|`_DOMAIN`|  
  
 `ceil` has an implementation that uses Streaming SIMD Extensions 2 (SSE2). For information and restrictions about using the SSE2 implementation, see [_set_SSE2_enable](../vs140/_set_SSE2_enable.md).  
  
## Remarks  
 Because C++ allows overloading, you can call overloads of `ceil`. In a C program, `ceil` always takes and returns a double.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`ceil`, `ceilf`, `ceill`|<math.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
 See the example for [floor](../vs140/floor--floorf--floorl.md).  
  
## .NET Framework Equivalent  
 [System::Math::Ceiling](https://msdn.microsoft.com/en-us/library/system.math.ceiling.aspx)  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [floor, floorf, floorl](../vs140/floor--floorf--floorl.md)   
 [fmod, fmodf](../vs140/fmod--fmodf.md)   
 [round](../vs140/round--roundf--roundl.md)