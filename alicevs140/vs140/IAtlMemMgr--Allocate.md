---
title: "IAtlMemMgr::Allocate"
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
ms.assetid: 2ae6de24-486b-4d25-ae8f-128eec86665e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAtlMemMgr::Allocate
Call this method to allocate a block of memory.  
  
## Syntax  
  
```  
  
      void* Allocate(  
   size_t nBytes   
) throw( );  
```  
  
#### Parameters  
 `nBytes`  
 The requested number of bytes in the new memory block.  
  
## Return Value  
 Returns a pointer to the start of the newly allocated memory block.  
  
## Remarks  
 Call [IAtlMemMgr::Free](../vs140/IAtlMemMgr--Free.md) or [IAtlMemMgr::Reallocate](../vs140/IAtlMemMgr--Reallocate.md) to free the memory allocated by this method.  
  
## Example  
 For an example, see the [IAtlMemMgr Overview](../vs140/IAtlMemMgr-Class.md).  
  
## Requirements  
 **Header:** atlmem.h  
  
## See Also  
 [IAtlMemMgr Class](../vs140/IAtlMemMgr-Class.md)