---
title: "CSimpleMap::ReverseLookup"
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
ms.assetid: c204e81b-e1e7-4d22-af98-beb4c1600d57
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleMap::ReverseLookup
Returns the key associated with the given value.  
  
## Syntax  
  
```  
  
      TKey ReverseLookup(  
   const TVal& val   
) const;  
```  
  
#### Parameters  
 *val*  
 The value.  
  
## Return Value  
 Returns the associated key. If no matching key is found, NULL is returned.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleMap Class](../vs140/CSimpleMap-Class.md)   
 [CSimpleMap::Lookup](../vs140/CSimpleMap--Lookup.md)