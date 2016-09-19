---
title: "__ull_rshift"
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
ms.assetid: b7ff5254-3540-4e6e-b57c-a6c4beb7dca2
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __ull_rshift
**Microsoft Specific**  
  
 on x64, shifts a 64-bit value specified by the first parameter to the right by a number of bits specified by the second parameter.  
  
## Syntax  
  
```  
unsigned __int64 __ull_rshift(   
   unsigned __int64 mask,    
   int nBit   
);  
```  
  
#### Parameters  
 [in] `mask`  
 The 64-bit integer value to shift right.  
  
 [in] `nBit`  
 The number of bits to shift, modulo 32 on x86, and modulo 64 on x64.  
  
## Return Value  
 The mask shifted by `nBit` bits.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__ull_rshift`|x86, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 If the second parameter is greater than 31 on x86 (63 on x64), that number is taken modulo 32 (64 on x64) to determine the number of bits to shift. The `ull` in the name indicates `unsigned long long (unsigned __int64)`.  
  
## Example  
  
```  
// ull_rshift.cpp  
// compile with: /EHsc  
// processor: x86, x64  
#include <iostream>  
#include <intrin.h>  
using namespace std;  
  
#pragma intrinsic(__ull_rshift)  
  
int main()  
{  
   unsigned __int64 mask = 0x100;  
   int nBit = 8;  
   mask = __ull_rshift(mask, nBit);  
   cout << hex << mask << endl;  
}  
```  
  
## Output  
  
```  
1  
```  
  
### END Microsoft Specific  
  
## See Also  
 [__ll_lshift](../vs140/__ll_lshift.md)   
 [__ll_rshift](../vs140/__ll_rshift.md)   
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)