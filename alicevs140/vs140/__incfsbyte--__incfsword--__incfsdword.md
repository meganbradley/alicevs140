---
title: "__incfsbyte, __incfsword, __incfsdword"
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
ms.assetid: 820457fb-e35e-42d3-bcb6-725da3281c64
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __incfsbyte, __incfsword, __incfsdword
**Microsoft Specific**  
  
 Add one to the value at a memory location specified by an offset relative to the beginning of the `FS` segment.  
  
## Syntax  
  
```  
void __incfsbyte(   
   unsigned long Offset   
);  
void __incfsword(   
   unsigned long Offset   
);  
void __incfsdword(   
   unsigned long Offset  
);  
```  
  
#### Parameters  
 [in] `Offset`  
 The offset from the beginning of `FS`.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__incfsbyte`|x86|  
|`__incfsword`|x86|  
|`__incfsdword`|x86|  
  
## Remarks  
 These intrinsics are only available in kernel mode, and the routines are only available as intrinsics.  
  
## END Microsoft Specific  
  
## See Also  
 [__addfsbyte, \__addfsword, \__adfsdword](../vs140/__addfsbyte--__addfsword--__addfsdword.md)   
 [__readfsbyte, \__readfsdword, \__readfsqword, \__readfsword](../vs140/__readfsbyte--__readfsdword--__readfsqword--__readfsword.md)   
 [__writefsbyte, \__writefsdword, \__writefsqword, \__writefsword](../vs140/__writefsbyte--__writefsdword--__writefsqword--__writefsword.md)   
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)