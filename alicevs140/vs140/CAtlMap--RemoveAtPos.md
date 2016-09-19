---
title: "CAtlMap::RemoveAtPos"
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
ms.assetid: c15fc734-4a39-4723-a1b6-65f7aa1de5ca
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::RemoveAtPos
Call this method to remove the element at the given position in the `CAtlMap` object.  
  
## Syntax  
  
```  
  
      void RemoveAtPos(  
   POSITION pos   
) throw( );  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to [CAtlMap::GetNextAssoc](../vs140/CAtlMap--GetNextAssoc.md) or [CAtlMap::GetStartPosition](../vs140/CAtlMap--GetStartPosition.md).  
  
## Remarks  
 Removes the key/value pair stored at the specified position. The memory used to store the element is freed. The POSITION referenced by `pos` becomes invalid, and while the POSITION of any other elements in the map remains valid, they do not necessarily retain the same order.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CAtlMap::RemoveKey](../vs140/CAtlMap--RemoveKey.md)   
 [CAtlMap::RemoveAll](../vs140/CAtlMap--RemoveAll.md)