---
title: "_status87, _statusfp, _statusfp2"
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
  - _statusfp2
  - _statusfp
  - _status87
apilocation: 
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 7ef963fa-b1fb-429d-94d6-fbf282ab7432
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _status87, _statusfp, _statusfp2
Gets the floating-point status word.  
  
## Syntax  
  
```  
unsigned int _status87( void );  
unsigned int _statusfp( void );  
void _statusfp2(unsigned int *px86, unsigned int *pSSE2)  
```  
  
#### Parameters  
 `px86`  
 This address is filled with the status word for the x87 floating-point unit.  
  
 `pSSE2`  
 This address is filled with the status word for the SSE2 floating-point unit.  
  
## Return Value  
 For `_status87` and `_statusfp`, the bits in the value that's returned indicate the floating-point status. See the FLOAT.H include file for a definition of the bits that are returned by `_statusfp`. Many math library functions modify the floating-point status word, with unpredictable results. Optimization can reorder, combine, and eliminate floating-point operations around calls to `_status87`, `_statusfp`, and related functions. Use the [/Od](../Topic/-Od%20\(Disable%20\(Debug\)\).md) compiler option or the [fenv_access](../vs140/fenv_access.md) pragma directive to prevent optimizations that reorder floating-point operations. Return values from `_clearfp` and `_statusfp`, and also the return parameters of `_statusfp2`, are more reliable if fewer floating-point operations are performed between known states of the floating-point status word.  
  
## Remarks  
 The `_statusfp` function gets the floating-point status word. The status word is a combination of the floating-point processor status and other conditions detected by the floating-point exception handler—for example, floating-point stack overflow and underflow. Unmasked exceptions are checked for before the contents of the status word are returned. This means that the caller is informed of pending exceptions. On x86 platforms, `_statusfp` returns a combination of the x87 and SSE2 floating-point status. On x64 platforms, the status that's returned is based on the SSE’s MXCSR status. On ARM platforms, `_statusfp` returns status from the FPSCR register.  
  
 `_statusfp` is a platform-independent, portable version of `_status87`. It is identical to `_status87` on Intel (x86) platforms and is also supported by the x64 and ARM platforms. To ensure that your floating-point code is portable to all architectures, use `_statusfp`. If you are only targeting x86 platforms, you can use either `_status87` or `_statusfp`.  
  
 We recommend `_statusfp2` for chips (such as the Pentium IV) that have both an x87 and an SSE2 floating-point processor. For `_statusfp2`, the addresses are filled by using the floating-point status word for both the x87 or the SSE2 floating-point processor. For a chip that supports x87 and SSE2 floating-point processors, EM_AMBIGUOUS is set to 1 if `_statusfp` or `_controlfp` is used and the action was ambiguous because it could refer to the x87 or the SSE2 floating-point status word. The `_statusfp2` function is only supported on x86 platforms.  
  
 These functions are not useful for [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) or `/clr:pure` compilation because the common language runtime (CLR) only supports the default floating-point precision.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_status87`, `_statusfp`, `_statusfp2`|<float.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_statusfp.c  
// Build by using: cl /W4 /Ox /nologo crt_statusfp.c  
// This program creates various floating-point errors and  
// then uses _statusfp to display messages that indicate these problems.  
  
#include <stdio.h>  
#include <float.h>  
#pragma fenv_access(on)  
  
double test( void )  
{  
   double a = 1e-40;  
   float b;  
   double c;  
  
   printf("Status = 0x%.8x - clear\n", _statusfp());  
  
   // Assignment into b is inexact & underflows:   
   b = (float)(a + 1e-40);  
   printf("Status = 0x%.8x - inexact, underflow\n", _statusfp());  
  
   // c is denormal:   
   c = b / 2.0;   
   printf("Status = 0x%.8x - inexact, underflow, denormal\n",   
            _statusfp());  
  
   // Clear floating point status:   
   _clearfp();  
   return c;  
}  
  
int main(void)  
{  
   return (int)test();  
}  
```  
  
 **Status = 0x00000000 - clear**  
**Status = 0x00000003 - inexact, underflow**  
**Status = 0x00080003 - inexact, underflow, denormal**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [_clear87, _clearfp](../vs140/_clear87--_clearfp.md)   
 [_control87, _controlfp, \__control87_2](../vs140/_control87--_controlfp--__control87_2.md)