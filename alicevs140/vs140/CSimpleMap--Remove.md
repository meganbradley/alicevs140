---
title: "CSimpleMap::Remove"
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
ms.assetid: a191c55e-a3f6-4eaa-9918-f14a2ebb75a1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleMap::Remove
Removes a key and matching value.  
  
## Syntax  
  
```  
  
      BOOL Remove(  
   const TKey& key   
);  
```  
  
#### Parameters  
 `key`  
 The key.  
  
## Return Value  
 Returns TRUE if the key, and matching value, were successfully removed, FALSE otherwise.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleMap Class](../vs140/CSimpleMap-Class.md)   
 [CSimpleMap::RemoveAll](../vs140/CSimpleMap--RemoveAll.md)   
 [CSimpleMap::RemoveAt](../vs140/CSimpleMap--RemoveAt.md)