---
title: "CRBMultiMap::Insert"
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
ms.assetid: 2f9229c4-f00e-4321-b32d-867514fe3ef0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBMultiMap::Insert
Call this method to insert an element pair into the map.  
  
## Syntax  
  
```  
  
      POSITION Insert(  
   KINARGTYPE key,  
   VINARGTYPE value  
) throw(...);  
```  
  
#### Parameters  
 `key`  
 The key value to add to the `CRBMultiMap` object.  
  
 *value*  
 The value to add to the `CRBMultiMap` object, associated with `key`.  
  
## Return Value  
 Returns the position of the key/value element pair in the `CRBMultiMap` object.  
  
## Remarks  
 See the documentation for the base class [CRBTree](../vs140/CRBTree-Class.md) for information on the other methods available.  
  
## Example  
 See the example for [CRBMultiMap::CRBMultiMap](../vs140/CRBMultiMap--CRBMultiMap.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBMultiMap Class](../vs140/CRBMultiMap-Class.md)   
 [CRBMultiMap::RemoveKey](../vs140/CRBMultiMap--RemoveKey.md)