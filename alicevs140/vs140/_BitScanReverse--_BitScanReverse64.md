---
title: "_BitScanReverse, _BitScanReverse64"
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
ms.assetid: 2520a207-af8b-4aad-9ae7-831abeadf376
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _BitScanReverse, _BitScanReverse64
**Microsoft Specific**  
  
 Search the mask data from most significant bit (MSB) to least significant bit (LSB) for a set bit (1).  
  
## Syntax  
  
```  
unsigned char _BitScanReverse(  
   unsigned long * Index,  
   unsigned long Mask  
);  
unsigned char _BitScanReverse64(  
   unsigned long * Index,  
   unsigned __int64 Mask  
);  
```  
  
#### Parameters  
 [out] `Index`  
 Loaded with the bit position of the first set bit (1) found.  
  
 [in] `Mask`  
 The 32-bit or 64-bit value to search.  
  
## Return Value  
 Nonzero if `Index` was set, or 0 if no set bits were found.  
  
## Requirements  
  
|Intrinsic|Architecture|Header|  
|---------------|------------------|------------|  
|`_BitScanReverse`|x86, ARM, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|<intrin.h>|  
|`_BitScanReverse64`|ARM, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]||  
  
## Example  
  
```  
// BitScanReverse.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <intrin.h>  
using namespace std;  
  
#pragma intrinsic(_BitScanReverse)  
  
int main()  
{  
   unsigned long mask = 0x1000;  
   unsigned long index;  
   unsigned char isNonzero;  
  
   cout << "Enter a positive integer as the mask: " << flush;  
   cin >> mask;  
   isNonzero = _BitScanReverse(&index, mask);  
   if (isNonzero)  
   {  
      cout << "Mask: " << mask << " Index: " << index << endl;  
   }  
   else  
   {  
      cout << "No set bits found.  Mask is zero." << endl;  
   }  
}  
```  
  
## Input  
  
```  
12  
```  
  
## Sample Output  
  
```  
Enter a positive integer as the mask:   
Mask: 12 Index: 3  
```  
  
### END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)