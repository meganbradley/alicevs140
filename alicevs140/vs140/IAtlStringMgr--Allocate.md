---
title: "IAtlStringMgr::Allocate"
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
ms.assetid: 37cc9acc-f83e-4e30-a09f-33a9b7b96cf9
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAtlStringMgr::Allocate
Allocates a new string data structure.  
  
## Syntax  
  
```  
  
      CStringData* Allocate(  
   int nAllocLength,  
   int nCharSize   
) throw( );  
```  
  
#### Parameters  
 `nAllocLength`  
 The number of characters in the new memory block.  
  
 `nCharSize`  
 The size (in bytes) of the character type used by the string manager.  
  
## Return Value  
 Returns a pointer to the newly allocated memory block.  
  
> [!NOTE]
>  Do not signal a failed allocation by throwing an exception. Instead, a failed allocation should be signaled by returning **NULL**.  
  
## Remarks  
 Call [IAtlStringMgr::Free](../vs140/IAtlStringMgr--Free.md) or [IAtlStringMgr::ReAllocate](../vs140/IAtlStringMgr--Reallocate.md) to free the memory allocated by this method.  
  
> [!NOTE]
>  For usage examples, see [Memory Management and CStringT](../vs140/Memory-Management-with-CStringT.md).  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [IAtlStringMgr Class](../vs140/IAtlStringMgr-Class.md)