---
title: "CAtlMap::RemoveKey"
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
ms.assetid: 59d8d1d0-fbed-4954-8c16-f643e5f06106
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::RemoveKey
Call this method to remove an element from the `CAtlMap` object, given the key.  
  
## Syntax  
  
```  
  
      bool RemoveKey(  
   KINARGTYPE key   
) throw( );  
```  
  
#### Parameters  
 `key`  
 The key corresponding to the element pair you want to remove.  
  
## Return Value  
 Returns **true** if the key is found and removed, **false** on failure.  
  
## Example  
 See the example for [CAtlMap::CAtlMap](../vs140/CAtlMap--CAtlMap.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CAtlMap::RemoveAll](../vs140/CAtlMap--RemoveAll.md)   
 [CAtlMap::RemoveAtPos](../vs140/CAtlMap--RemoveAtPos.md)