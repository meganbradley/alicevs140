---
title: "__outbytestring"
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
ms.assetid: c9150661-9c18-427f-bae8-710bba6ed78c
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __outbytestring
**Microsoft Specific**  
  
 Generates the `rep outsb` instruction,which sends the first `Count` bytes of data pointed to by `Buffer` to the port specified by `Port`.  
  
## Syntax  
  
```  
void __outbytestring(   
   unsigned short Port,   
   unsigned char* Buffer,   
   unsigned long Count   
);  
```  
  
#### Parameters  
 [in] `Port`  
 The port to send the data to.  
  
 [in] `Buffer`  
 The data to be sent out the specified port.  
  
 [in] `Count`  
 The number of bytes of data to be sent.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__outbytestring`|x86, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 This routine is only available as an intrinsic.  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)