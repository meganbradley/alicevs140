---
title: "CAtlMap::SetAt"
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
ms.assetid: c909fc7b-f6ea-4903-b536-2395dd6bed44
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::SetAt
Call this method to insert an element pair into the map.  
  
## Syntax  
  
```  
  
      POSITION SetAt(  
   KINARGTYPE key,  
   VINARGTYPE value   
);  
```  
  
#### Parameters  
 `key`  
 The key value to add to the `CAtlMap` object.  
  
 *value*  
 The value to add to the `CAtlMap` object.  
  
## Return Value  
 Returns the position of the key/value element pair in the `CAtlMap` object.  
  
## Remarks  
 `SetAt` replaces an existing element if a matching key is found. If the key is not found, a new key/value pair is created.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CAtlMap::SetValueAt](../vs140/CAtlMap--SetValueAt.md)