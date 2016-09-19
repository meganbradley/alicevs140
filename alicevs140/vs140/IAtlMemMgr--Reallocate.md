---
title: "IAtlMemMgr::Reallocate"
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
ms.assetid: 2e2696ac-5b43-40c5-b41d-63122ee794f0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAtlMemMgr::Reallocate
Call this method to reallocate memory allocated by this memory manager.  
  
## Syntax  
  
```  
  
      void* Reallocate(  
   void* p,  
   size_t nBytes   
) throw( );  
```  
  
#### Parameters  
 `p`  
 Pointer to memory previously allocated by this memory manager.  
  
 `nBytes`  
 The requested number of bytes in the new memory block.  
  
## Return Value  
 Returns a pointer to the start of the newly allocated memory block.  
  
## Remarks  
 Call [IAtlMemMgr::Free](../vs140/IAtlMemMgr--Free.md) or [IAtlMemMgr::Reallocate](#vclrfiatlmemmgrreallocate) to free the memory allocated by this method.  
  
 Conceptually this method frees the existing memory and allocates a new memory block. In reality, the existing memory may be extended or otherwise reused.  
  
## Example  
 For an example, see the [IAtlMemMgr Overview](../vs140/IAtlMemMgr-Class.md).  
  
## Requirements  
 **Header:** atlmem.h  
  
## See Also  
 [IAtlMemMgr Class](../vs140/IAtlMemMgr-Class.md)