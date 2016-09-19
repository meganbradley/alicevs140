---
title: "IAtlMemMgr::GetSize"
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
ms.assetid: 0125c67e-401b-4390-bf72-8d19f11c67a4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAtlMemMgr::GetSize
Call this method to retrieve the size of an allocated memory block.  
  
## Syntax  
  
```  
  
      size_t GetSize(  
   void* p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 Pointer to memory previously allocated by this memory manager.  
  
## Return Value  
 Returns the size of the memory block in bytes.  
  
## Example  
 For an example, see the [IAtlMemMgr Overview](../vs140/IAtlMemMgr-Class.md).  
  
## Requirements  
 **Header:** atlmem.h  
  
## See Also  
 [IAtlMemMgr Class](../vs140/IAtlMemMgr-Class.md)