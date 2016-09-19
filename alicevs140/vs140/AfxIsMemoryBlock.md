---
title: "AfxIsMemoryBlock"
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
ms.assetid: 2273be29-8955-4859-9711-21d6cbff893b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxIsMemoryBlock
Tests a memory address to make sure it represents a currently active memory block that was allocated by the diagnostic version of **new**.  
  
## Syntax  
  
```  
  
      BOOL AfxIsMemoryBlock(  
   const void* p,  
   UINT nBytes,  
   LONG* plRequestNumber = NULL   
);  
```  
  
#### Parameters  
 `p`  
 Points to the block of memory to be tested.  
  
 `nBytes`  
 Contains the length of the memory block in bytes.  
  
 `plRequestNumber`  
 Points to a **long** integer that will be filled in with the memory block's allocation sequence number, or zero if it does not represent a currently active memory block.  
  
## Return Value  
 Nonzero if the memory block is currently allocated and the length is correct; otherwise 0.  
  
## Remarks  
 It also checks the specified size against the original allocated size. If the function returns nonzero, the allocation sequence number is returned in `plRequestNumber`. This number represents the order in which the block was allocated relative to all other **new** allocations.  
  
## Example  
 [!CODE [NVC_MFC_Utilities#27](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#27)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxIsValidAddress](../vs140/AfxIsValidAddress.md)