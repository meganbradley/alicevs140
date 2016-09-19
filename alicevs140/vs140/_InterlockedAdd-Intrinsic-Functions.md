---
title: "_InterlockedAdd Intrinsic Functions"
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
ms.assetid: 3d319603-ea9c-4fdd-ae61-e52430ccc3b1
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _InterlockedAdd Intrinsic Functions
**Microsoft Specific**  
  
 Perform an atomic addition, which ensures that the operation completes successfully when multiple threads have access to a shared variable.  
  
## Syntax  
  
```  
long _InterlockedAdd(  
   long volatile * Addend,  
   long Value  
);  
long _InterlockedAdd_acq(  
   long volatile * Addend,  
   long Value  
);  
long _InterlockedAdd_nf(  
   long volatile * Addend,  
   long Value  
);  
long _InterlockedAdd_rel(  
   long volatile * Addend,  
   long Value  
);  
__int64 _InterlockedAdd64(  
   __int64 volatile * Addend,  
   __int64 Value  
);  
__int64 _InterlockedAdd64_acq(  
   __int64 volatile * Addend,  
   __int64 Value  
);  
__int64 _InterlockedAdd64_nf (  
   __int64 volatile * Addend,  
   __int64 Value  
);  
__int64 _InterlockedAdd64_rel(  
   __int64 volatile * Addend,  
   __int64 Value  
);  
```  
  
#### Parameters  
 [in, out] `Addend`  
 Pointer to the integer to be added to; replaced by the result of the addition.  
  
 [in] `Value`  
 The value to add.  
  
## Return Value  
 Both functions return the result of the addition.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`_InterlockedAdd`|ARM|  
|`_InterlockedAdd_acq`|ARM|  
|`_InterlockedAdd_nf`|ARM|  
|`_InterlockedAdd_rel`|ARM|  
|`_InterlockedAdd64`|ARM|  
|`_InterlockedAdd64_acq`|ARM|  
|`_InterlockedAdd64_nf`|ARM|  
|`_InterlockedAdd64_rel`|ARM|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 The versions of these functions with the `_acq` or `_rel` suffixes perform an interlocked addition following acquire or release semantics. Acquire semantics means that the result of the operation are made visible to all threads and processors before any subsequent memory reads and writes. Acquire is useful when entering a critical section. Release semantics means that all memory reads and writes are forced to be made visible to all threads and processors before the result of the operation is made visible itself. Release is useful when leaving a critical section. The intrinsics with an `_nf` ("no fence") suffix do not act as a memory barrier.  
  
 These routines are only available as intrinsics.  
  
## Example  
  
```  
// interlockedadd.cpp  
// Compile with: /Oi /EHsc  
// processor: ARM  
#include <stdio.h>  
#include <intrin.h>  
  
#pragma intrinsic(_InterlockedAdd)  
  
int main()  
{  
        long data1 = 0xFF00FF00;  
        long data2 = 0x00FF0000;  
        long retval;  
        retval = _InterlockedAdd(&data1, data2);  
        printf("0x%x 0x%x 0x%x", data1, data2, retval);  
}  
```  
  
## Output  
  
```  
0xffffff00 0xff0000 0xffffff00  
```  
  
## Example  
  
```  
// interlockedadd64.cpp  
// compile with: /Oi /EHsc  
// processor: ARM  
#include <iostream>  
#include <intrin.h>  
using namespace std;  
  
#pragma intrinsic(_InterlockedAdd64)  
  
int main()  
{  
        __int64 data1 = 0x0000FF0000000000;  
        __int64 data2 = 0x00FF0000FFFFFFFF;  
        __int64 retval;  
        cout << hex << data1 << " + " << data2 << " = " ;  
        retval = _InterlockedAdd64(&data1, data2);  
        cout << data1 << endl;  
        cout << "Return value: " << retval << endl;  
}  
```  
  
## Output  
  
```  
ff0000000000 + ff0000ffffffff = ffff00ffffffff  
Return value: ffff00ffffffff  
```  
  
### END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)   
 [Conflicts with the x86 Compiler](../vs140/Conflicts-with-the-x86-Compiler.md)