---
title: "__inbytestring"
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
ms.assetid: fe549556-e7a3-4af3-8ebf-8a7dc3cb233b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __inbytestring
**Microsoft Specific**  
  
 Reads data from the specified port using the `rep insb` instruction.  
  
## Syntax  
  
```  
void __inbytestring(  
   unsigned short Port,  
   unsigned char* Buffer,  
   unsigned long Count  
);  
```  
  
#### Parameters  
 [in] `Port`  
 The port to read from.  
  
 [out] `Buffer`  
 The data read from the port is written here.  
  
 [in] `Count`  
 The number of bytes of data to read.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__inbytestring`|x86, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 This routine is only available as an intrinsic.  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)