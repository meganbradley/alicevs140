---
title: "_mm_cvtss_si64x"
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
ms.assetid: c279aff2-ee29-4271-8829-3ec691bf7718
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _mm_cvtss_si64x
**Microsoft Specific**  
  
 Generates the [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)] extended version of the Convert Scalar Single Precision Floating Point Number to 64-bit Integer (`cvtss2si`) instruction.  
  
## Syntax  
  
```  
__int64 _mm_cvtss_si64x(   
   __m128 value   
);  
```  
  
#### Parameters  
 [in] `value`  
 An `__m128` structure containing floating point-values.  
  
## Return Value  
 A 64-bit integer, the result of the conversion of the first floating-point value to an integer.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`_mm_cvtss_si64x`|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 The first element of the structure value is converted to an integer and returned. The rounding control bits in MXCSR are used to determine the rounding behavior. The default rounding mode is round to nearest, rounding to the even number if the decimal part is 0.5. Because the `__m128` structure represents an XMM register, this intrinsic takes a value from the XMM register and writes it to system memory.  
  
 This routine is only available as an intrinsic.  
  
## Example  
  
```  
// _mm_cvtss_si64x.cpp  
// processor: x64  
#include <intrin.h>  
#include <stdio.h>  
  
#pragma intrinsic(_mm_cvtss_si64x)  
  
int main()  
{  
    __m128 a;  
    __int64 b = 54;  
  
    // _mm_load_ps requires an aligned buffer.  
    __declspec(align(16)) float af[4] =  
                           { 101.25, 200.75, 300.5, 400.5 };  
  
    // Load a with the floating point values.  
    // The values will be copied to the XMM registers.  
    a = _mm_load_ps(af);  
  
    // Extract the first element of a and convert to an integer  
    b = _mm_cvtss_si64x(a);  
  
    printf_s("%I64d\n", b);  
}  
```  
  
 **101**   
## END Microsoft Specific  
  
## See Also  
 [__m128d](../vs140/__m128d.md)   
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)