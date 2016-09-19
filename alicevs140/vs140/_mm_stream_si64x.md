---
title: "_mm_stream_si64x"
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
ms.assetid: 114c2cd0-085f-41aa-846e-87bdd56c9ee7
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _mm_stream_si64x
**Microsoft Specific**  
  
 Generates the MOVNTI instruction. Writes the data in `Source` to a memory location specified by `Dest`, without polluting the caches.  
  
## Syntax  
  
```  
void _mm_stream_si64x(   
   __int64 * Dest,   
   __int64 Source   
);  
```  
  
#### Parameters  
 [out] `Dest`  
 A pointer to the location to write the source data to.  
  
 [in] `Source`  
 The data to write.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`_mm_stream_si64x`|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 This routine is only available as an intrinsic.  
  
## Example  
  
```  
// _mm_stream_si64x.c  
// processor: x64  
  
#include <stdio.h>  
#include <intrin.h>  
  
#pragma intrinsic(_mm_stream_si64x)  
  
int main()  
{  
    __int64 val = 0xFFFFFFFFFFFFI64;  
    __int64 a[10];  
  
    memset(a, 0, sizeof(a));  
    _mm_stream_si64x(a+1, val);  
    printf_s( "%I64x %I64x %I64x %I64x", a[0], a[1], a[2], a[3]);   
}  
```  
  
 **0 ffffffffffff 0 0**   
## END Microsoft Specific  
  
## See Also  
 [Cache Support for Streaming SIMD Extensions 2 Integer Operations](assetId:///a9c9b42f-de9e-4374-aeb6-5f65bfb669b6)   
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)