---
title: "__readfsbyte, __readfsdword, __readfsqword, __readfsword"
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
ms.assetid: f6ee7203-4179-402c-a464-0746c84ce6ac
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __readfsbyte, __readfsdword, __readfsqword, __readfsword
**Microsoft Specific**  
  
 Read memory from a location specified by an offset relative to the beginning of the FS segment.  
  
## Syntax  
  
```  
unsigned char __readfsbyte(   
   unsigned long Offset   
);  
unsigned short __readfsword(   
   unsigned long Offset   
);  
unsigned long __readfsdword(   
   unsigned long Offset  
);  
unsigned __int64 __readfsqword(   
   unsigned long Offset   
);  
```  
  
#### Parameters  
 [in] `Offset`  
 The offset from the beginning of `FS` to read from.  
  
## Return Value  
 The memory contents of the byte, word, doubleword, or quadword (as indicated by the name of the function called) at the location `FS:[``Offset``]`.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__readfsbyte`|x86|  
|`__readfsdword`|x86|  
|`__readfsqword`|x86|  
|`__readfsword`|x86|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 These routines are available only as intrinsics.  
  
## END Microsoft Specific  
  
## See Also  
 [__writefsbyte, \__writefsdword, \__writefsqword, \__writefsword](../vs140/__writefsbyte--__writefsdword--__writefsqword--__writefsword.md)   
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)