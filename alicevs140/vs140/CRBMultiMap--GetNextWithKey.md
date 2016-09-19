---
title: "CRBMultiMap::GetNextWithKey"
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
ms.assetid: d8c77386-64d9-42c4-96ce-14a45a44e595
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBMultiMap::GetNextWithKey
Call this method to get the element associated with a given key and update the position value.  
  
## Syntax  
  
```  
  
      const CPair* GetNextWithKey(  
   POSITION& pos,  
   KINARGTYPE key   
) const throw( );  
CPair* GetNextWithKey(  
   POSITION& pos,  
   KINARGTYPE key   
) throw( );  
```  
  
#### Parameters  
 `pos`  
 The position value, obtained with either a call to [CRBMultiMap::FindFirstWithKey](../vs140/CRBMultiMap--FindFirstWithKey.md) or [CRBMultiMap::GetNextValueWithKey](../vs140/CRBMultiMap--GetNextValueWithKey.md), or a previous call to `GetNextWithKey`.  
  
 `key`  
 Specifies the key that identifies the element to be found.  
  
## Return Value  
 Returns the next [CRBTree::CPair Class](../vs140/CRBTree--CPair-Class.md) element associated with the given key.  
  
## Remarks  
 The position value is updated to point to the next value associated with the key. If no more values exist, the position value is set to NULL.  
  
 See the documentation for the base class [CRBTree](../vs140/CRBTree-Class.md) for information on the other methods available.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBMultiMap Class](../vs140/CRBMultiMap-Class.md)   
 [CRBMultiMap::FindFirstWithKey](../vs140/CRBMultiMap--FindFirstWithKey.md)   
 [CRBMultiMap::GetNextValueWithKey](../vs140/CRBMultiMap--GetNextValueWithKey.md)