---
title: "CAtlMap::GetNextValue"
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
ms.assetid: 9efeb96b-52a7-45aa-97ab-03ad3773b53e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::GetNextValue
Call this method to get the next value from the `CAtlMap` object.  
  
## Syntax  
  
```  
  
      V& GetNextValue(  
   POSITION& pos   
) throw( );  
const V& GetNextValue(  
   POSITION& pos   
) const throw( );  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to [CAtlMap::GetNextAssoc](../vs140/CAtlMap--GetNextAssoc.md) or [CAtlMap::GetStartPosition](../vs140/CAtlMap--GetStartPosition.md).  
  
## Return Value  
 Returns a reference to the next value in the map.  
  
## Remarks  
 Updates the current position counter, `pos`. If there are no more entries in the map, the position counter is set to NULL.  
  
## Example  
 See the example for [CAtlMap::CAtlMap](../vs140/CAtlMap--CAtlMap.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CAtlMap::GetNext](../vs140/CAtlMap--GetNext.md)   
 [CAtlMap::GetNextKey](../vs140/CAtlMap--GetNextKey.md)   
 [CAtlMap::GetNextAssoc](../vs140/CAtlMap--GetNextAssoc.md)