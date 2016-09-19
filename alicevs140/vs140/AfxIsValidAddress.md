---
title: "AfxIsValidAddress"
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
ms.assetid: 9ed7dcac-f3fd-4e57-aa08-4e8683bcfd45
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxIsValidAddress
Tests any memory address to ensure that it is contained entirely within the program's memory space.  
  
## Syntax  
  
```  
  
      BOOL AfxIsValidAddress(  
   const void* lp,  
   UINT nBytes,  
   BOOL bReadWrite = TRUE   
);   
```  
  
#### Parameters  
 `lp`  
 Points to the memory address to be tested.  
  
 `nBytes`  
 Contains the number of bytes of memory to be tested.  
  
 *bReadWrite*  
 Specifies whether the memory is both for reading and writing (**TRUE**) or just reading (**FALSE**).  
  
## Return Value  
 In debug builds, nonzero if the specified memory block is contained entirely within the program's memory space; otherwise 0.  
  
 In non-debug builds, nonzero if `lp` is not NULL; otherwise 0.  
  
## Remarks  
 The address is not restricted to blocks allocated by **new**.  
  
## Example  
 [!CODE [NVC_MFC_Utilities#28](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#28)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxIsMemoryBlock](../vs140/AfxIsMemoryBlock.md)   
 [AfxIsValidString](../vs140/AfxIsValidString.md)