---
title: "IAtlStringMgr::Reallocate"
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
ms.topic: reference
ms.assetid: a0a6b13f-2f25-4786-9ea8-89ed494c05ef
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAtlStringMgr::Reallocate
Reallocates a string data structure.  
  
## Syntax  
  
```  
  
      CStringData* Reallocate(  
   CStringData* pData,  
   int nAllocLength,  
   int nCharSize   
) throw( );  
```  
  
#### Parameters  
 `pData`  
 Pointer to the memory previously allocated by this memory manager.  
  
 `nAllocLength`  
 The number of characters in the new memory block.  
  
 `nCharSize`  
 The size (in bytes) of the character type used by the string manager.  
  
## Return Value  
 Returns a pointer to the start of the newly allocated memory block.  
  
## Remarks  
 Call this function to resize the existing memory block specified by `pData`.  
  
 Call [IAtlStringMgr::Free](../vs140/IAtlStringMgr--Free.md) to free the memory allocated by this method.  
  
> [!NOTE]
>  For usage examples, see [Memory Management and CStringT](../vs140/Memory-Management-with-CStringT.md).  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [IAtlStringMgr Class](../vs140/IAtlStringMgr-Class.md)