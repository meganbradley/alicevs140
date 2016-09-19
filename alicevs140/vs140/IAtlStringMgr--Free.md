---
title: "IAtlStringMgr::Free"
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
ms.assetid: 7e806d9f-b2dc-4208-99a1-223f2393c786
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAtlStringMgr::Free
Frees a string data structure.  
  
## Syntax  
  
```  
  
      void Free(  
   CStringData* pData   
) throw( );  
```  
  
#### Parameters  
 `pData`  
 A pointer to the memory block to be freed.  
  
## Remarks  
 Frees the specified memory block previously allocated by [Allocate](../vs140/IAtlStringMgr--Allocate.md) or [Reallocate](../vs140/IAtlMemMgr--Reallocate.md).  
  
> [!NOTE]
>  For usage examples, see [Memory Management and CStringT](../vs140/Memory-Management-with-CStringT.md).  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [IAtlStringMgr Class](../vs140/IAtlStringMgr-Class.md)   
 [IAtlStringMgr::Free](../vs140/IAtlStringMgr--Free.md)