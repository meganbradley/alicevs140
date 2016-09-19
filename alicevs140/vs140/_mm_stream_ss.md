---
title: "_mm_stream_ss"
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
ms.assetid: c53dffe9-0dfe-4063-85d3-e8987b870fce
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _mm_stream_ss
**Microsoft Specific**  
  
 Writes 32-bit data to a memory location without polluting the caches.  
  
## Syntax  
  
```  
void _mm_stream_ss(  
   float * Dest,  
   __m128 Source  
);  
```  
  
#### Parameters  
 [out] `Dest`  
 A pointer to the location where the source data is written.  
  
 [in] `Source`  
 A 128-bit number that contains the `float` value to be written in its bottom 32 bits..  
  
## Return Value  
 None.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`_mm_stream_ss`|SSE4a|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 This intrinsic generates the `movntss` instruction. To determine hardware support for this instruction, call the `__cpuid` intrinsic with `InfoType=0x80000001`and check bit 6 of `CPUInfo[2] (ECX)`. This bit is 1 when the instruction is supported, and 0 otherwise.  
  
 If you run code that uses the `_mm_stream_ss` intrinsic on hardware that does not support the `movntss` instruction, the results are unpredictable.  
  
## Example  
  
```  
// Compile this sample with: /EHsc  
#include <iostream>  
#include <intrin.h>  
using namespace std;  
  
int main()  
{  
    __m128 vals;  
    float f[4];  
  
    f[0] = -1.;  
    f[1] = -2.;  
    f[2] = -3.;  
    f[3] = -4.;  
    vals.m128_f32[0] = 0.;  
    vals.m128_f32[1] = 1.;  
    vals.m128_f32[2] = 2.;  
    vals.m128_f32[3] = 3.;  
    _mm_stream_ss(&f[3], vals);  
    cout << "f[0] = " << f[0] << ", f[1] = " << f[1] << endl;  
    cout << "f[1] = " << f[1] << ", f[3] = " << f[3] << endl;  
}  
  
```  
  
 **f[0] = -1, f[1] = -2**  
**f[2] = -3, f[3] = 3**   
## END Microsoft Specific  
 Copyright 2007 by Advanced Micro Devices, Inc. All rights reserved. Reproduced with permission from Advanced Micro Devices, Inc.  
  
## See Also  
 [_mm_stream_sd](../vs140/_mm_stream_sd.md)   
 [_mm_stream_ps](assetId:///f7af2f19-c0d4-43c6-b5f6-a658d2b1d869)   
 [_mm_store_ss](assetId:///dfeeea35-8faf-4f54-8a9e-6723e226fb08)   
 [_mm_sfence](assetId:///b6c0d18e-3628-4318-826b-45f66782e870)   
 [Streaming SIMD Extensions that Support the Cache](assetId:///8f03493a-d5f5-4457-892e-0b6540494872)   
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)