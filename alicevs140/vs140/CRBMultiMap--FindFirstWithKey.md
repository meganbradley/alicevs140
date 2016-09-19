---
title: "CRBMultiMap::FindFirstWithKey"
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
ms.assetid: 47e089fd-274f-483c-b540-42452720f9ab
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBMultiMap::FindFirstWithKey
Call this method to find the position of the first element with a given key.  
  
## Syntax  
  
```  
  
      POSITION FindFirstWithKey(  
   KINARGTYPE key   
) const throw( );  
```  
  
#### Parameters  
 `key`  
 Specifies the key that identifies the element to be found.  
  
## Return Value  
 Returns the POSITION of the first key/value element if the key is found, NULL otherwise.  
  
## Remarks  
 A key in the `CRBMultiMap` can have one or more associated values. This method will provide the position value of the first value (which may, in fact, be the only value) associated with that particular key. The position value returned can then be used with [CRBMultiMap::GetNextValueWithKey](../vs140/CRBMultiMap--GetNextValueWithKey.md) or [CRBMultiMap::GetNextWithKey](../vs140/CRBMultiMap--GetNextWithKey.md) to obtain the value and update the position.  
  
 See the documentation for the base class [CRBTree](../vs140/CRBTree-Class.md) for information on the other methods available.  
  
## Example  
 See the example for [CRBMultiMap::CRBMultiMap](../vs140/CRBMultiMap--CRBMultiMap.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBMultiMap Class](../vs140/CRBMultiMap-Class.md)   
 [CRBMultiMap::GetNextValueWithKey](../vs140/CRBMultiMap--GetNextValueWithKey.md)   
 [CRBMultiMap::GetNextWithKey](../vs140/CRBMultiMap--GetNextWithKey.md)