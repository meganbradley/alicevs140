---
title: "CAtlMap::GetNext"
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
ms.assetid: b7e623f0-ad55-49ba-9459-16282c103d1e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::GetNext
Call this method to obtain a pointer to the next element pair stored in the `CAtlMap` object.  
  
## Syntax  
  
```  
  
      CPair* GetNext(  
   POSITION& pos   
) throw( );  
const CPair* GetNext(  
   POSITION& pos   
) const throw( );  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to [CAtlMap::GetNextAssoc](../vs140/CAtlMap--GetNextAssoc.md) or [CAtlMap::GetStartPosition](../vs140/CAtlMap--GetStartPosition.md).  
  
## Return Value  
 Returns a pointer to the next pair of key/value elements stored in the map. The `pos` position counter is updated after each call. If the retrieved element is the last in the map, `pos` is set to NULL.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CAtlMap::GetNextAssoc](../vs140/CAtlMap--GetNextAssoc.md)   
 [CAtlMap::GetNextKey](../vs140/CAtlMap--GetNextKey.md)   
 [CAtlMap::GetNextValue](../vs140/CAtlMap--GetNextValue.md)   
 [CAtlMap::CPair Class](../vs140/CAtlMap--CPair-Class.md)