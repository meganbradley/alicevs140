---
title: "CAtlMap::GetNextKey"
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
ms.assetid: 5d7146ce-c526-4095-b5c9-c2ee7cfff87a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::GetNextKey
Call this method to retrieve the next key from the `CAtlMap` object.  
  
## Syntax  
  
```  
  
      const K& GetNextKey(  
   POSITION& pos   
) const throw( );  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to [CAtlMap::GetNextAssoc](../vs140/CAtlMap--GetNextAssoc.md) or [CAtlMap::GetStartPosition](../vs140/CAtlMap--GetStartPosition.md).  
  
## Return Value  
 Returns a reference to the next key in the map.  
  
## Remarks  
 Updates the current position counter, `pos`. If there are no more entries in the map, the position counter is set to NULL.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CAtlMap::GetNextValue](../vs140/CAtlMap--GetNextValue.md)   
 [CAtlMap::GetNext](../vs140/CAtlMap--GetNext.md)   
 [CAtlMap::GetNextAssoc](../vs140/CAtlMap--GetNextAssoc.md)