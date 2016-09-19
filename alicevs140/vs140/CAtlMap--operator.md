---
title: "CAtlMap::operator"
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
ms.assetid: 17bd98b6-b60a-4421-8b83-54329aec2dee
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::operator
Replaces or adds a new element to the `CAtlMap`.  
  
## Syntax  
  
```  
  
      V& operator[](KINARGTYPE key) throw( );  
```  
  
#### Parameters  
 `key`  
 The key of the element to add or replace.  
  
## Return Value  
 Returns a reference to the value associated with the given key.  
  
## Example  
 If the key already exists, the element is replaced. If the key does not exist, a new element is added. See the example for [CAtlMap::CAtlMap](../vs140/CAtlMap--CAtlMap.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CAtlMap::SetAt](../vs140/CAtlMap--SetAt.md)