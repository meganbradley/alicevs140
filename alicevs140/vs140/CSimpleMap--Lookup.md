---
title: "CSimpleMap::Lookup"
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
ms.assetid: 2c828d0e-4cc4-4d30-b114-55ec40d93f94
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleMap::Lookup
Returns the value associated with the given key.  
  
## Syntax  
  
```  
  
      TVal Lookup(  
   const TKey& key   
) const;  
```  
  
#### Parameters  
 `key`  
 The key.  
  
## Return Value  
 Returns the associated value. If no matching key is found, NULL is returned.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleMap Class](../vs140/CSimpleMap-Class.md)   
 [CSimpleMap::ReverseLookup](../vs140/CSimpleMap--ReverseLookup.md)