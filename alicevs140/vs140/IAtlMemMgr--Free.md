---
title: "IAtlMemMgr::Free"
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
ms.assetid: 63e3a6ea-7c25-4f84-aa01-2c649129b12c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAtlMemMgr::Free
Call this method to free a block of memory.  
  
## Syntax  
  
```  
  
      void Free(  
   void* p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 Pointer to memory previously allocated by this memory manager.  
  
## Remarks  
 Use this method to free memory obtained by [IAtlMemMgr::Allocate](../vs140/IAtlMemMgr--Allocate.md) or [IAtlMemMgr::Reallocate](../vs140/IAtlMemMgr--Reallocate.md).  
  
## Example  
 For an example, see the [IAtlMemMgr Overview](../vs140/IAtlMemMgr-Class.md).  
  
## Requirements  
 **Header:** atlmem.h  
  
## See Also  
 [IAtlMemMgr Class](../vs140/IAtlMemMgr-Class.md)