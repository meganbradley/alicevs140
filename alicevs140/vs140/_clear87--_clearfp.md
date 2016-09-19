---
title: "_clear87, _clearfp"
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
  - _clearfp
  - _clear87
apilocation: 
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcrt.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 72d24a70-7688-4793-ae09-c96d33fcca52
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _clear87, _clearfp
Gets and clears the floating-point status word.  
  
## Syntax  
  
```  
unsigned int _clear87( void );  
unsigned int _clearfp( void );  
```  
  
## Return Value  
 The bits in the value returned indicate the floating-point status before the call to `_clear87` or `_clearfp`. For a complete definition of the bits returned by `_clear87`, see Float.h. Many of the math library functions modify the 8087/80287 status word, with unpredictable results. Return values from `_clear87` and `_status87` become more reliable as fewer floating-point operations are performed between known states of the floating-point status word.  
  
## Remarks  
 The `_clear87` function clears the exception flags in the floating-point status word, sets the busy bit to 0, and returns the status word. The floating-point status word is a combination of the 8087/80287 status word and other conditions detected by the 8087/80287 exception handler, such as floating-point stack overflow and underflow.  
  
 `_clearfp` is a platform-independent, portable version of the `_clear87` routine. It is identical to `_clear87` on Intel (x86) platforms and is also supported by the x64 and ARM platforms. To ensure that your floating-point code is portable to x64 and ARM, use `_clearfp`. If you are only targeting x86 platforms, you can use either `_clear87` or `_clearfp`.  
  
 These functions are deprecated when compiling with [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) or `/clr:pure` because the common language runtime only supports the default floating-point precision.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_clear87`|<float.h>|  
|`_clearfp`|<float.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_clear87.c  
// compile with: /Od  
  
// This program creates various floating-point   
// problems, then uses _clear87 to report on these problems.  
// Compile this program with Optimizations disabled (/Od).   
// Otherwise the optimizer will remove the code associated with   
// the unused floating-point values.  
//  
  
#include <stdio.h>  
#include <float.h>  
  
int main( void )  
{  
   double a = 1e-40, b;  
   float x, y;  
  
   printf( "Status: %.4x - clear\n", _clear87()  );  
  
   // Store into y is inexact and underflows:  
   y = a;  
   printf( "Status: %.4x - inexact, underflow\n", _clear87() );  
  
   // y is denormal:   
   b = y;  
   printf( "Status: %.4x - denormal\n", _clear87() );  
}  
```  
  
 **Status: 0000 - clear**  
**Status: 0003 - inexact, underflow**  
**Status: 80000 - denormal**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [_control87, _controlfp, \__control87_2](../vs140/_control87--_controlfp--__control87_2.md)   
 [_status87, _statusfp, _statusfp2](../vs140/_status87--_statusfp--_statusfp2.md)