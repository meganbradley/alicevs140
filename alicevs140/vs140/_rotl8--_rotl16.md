---
title: "_rotl8, _rotl16"
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
ms.assetid: 8c519ab6-aef9-4f07-a387-daee8408368f
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _rotl8, _rotl16
**Microsoft Specific**  
  
 Rotate the input values to the left to the most significant bit (MSB) by a specified number of bit positions.  
  
## Syntax  
  
```  
unsigned char _rotl8(   
   unsigned char value,   
   unsigned char shift   
);  
unsigned short _rotl16(   
   unsigned short value,   
   unsigned char shift   
);  
```  
  
#### Parameters  
 [in] `value`  
 The value to rotate.  
  
 [in] `shift`  
 The number of bits to rotate.  
  
## Return Value  
 The rotated value.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`_rotl8`|x86, ARM, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
|`_rotl16`|x86, ARM, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 Unlike a left-shift operation, when executing a left rotation, the high order bits that fall off the high end are moved into the least significant bit positions.  
  
## Example  
  
```  
// rotl.cpp  
#include <stdio.h>  
#include <intrin.h>  
  
#pragma intrinsic(_rotl8, _rotl16)  
  
int main()  
{  
    unsigned char c = 'A', c1, c2;  
  
    for (int i = 0; i < 8; i++)  
    {  
       printf_s("Rotating 0x%x left by %d bits gives 0x%x\n", c,  
               i, _rotl8(c, i));  
    }  
  
    unsigned short s = 0x12;  
    int nBit = 10;  
  
    printf_s("Rotating unsigned short 0x%x left by %d bits gives 0x%x\n",  
            s, nBit, _rotl16(s, nBit));  
}  
```  
  
 **Rotating 0x41 left by 0 bits gives 0x41**  
**Rotating 0x41 left by 1 bits gives 0x82**  
**Rotating 0x41 left by 2 bits gives 0x5**  
**Rotating 0x41 left by 3 bits gives 0xa**  
**Rotating 0x41 left by 4 bits gives 0x14**  
**Rotating 0x41 left by 5 bits gives 0x28**  
**Rotating 0x41 left by 6 bits gives 0x50**  
**Rotating 0x41 left by 7 bits gives 0xa0**  
**Rotating unsigned short 0x12 left by 10 bits gives 0x4800**   
## END Microsoft Specific  
  
## See Also  
 [_rotr8, _rotr16](../vs140/_rotr8--_rotr16.md)   
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)