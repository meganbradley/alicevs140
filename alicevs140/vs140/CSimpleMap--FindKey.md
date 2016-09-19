---
title: "CSimpleMap::FindKey"
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
ms.assetid: ad1d0478-6835-4713-90e2-c279ccdccc35
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleMap::FindKey
Finds a specific key.  
  
## Syntax  
  
```  
  
      int FindKey(  
   const TKey& key   
) const;  
```  
  
#### Parameters  
 `key`  
 The key to search for.  
  
## Return Value  
 Returns the index of the key if found, otherwise returns -1.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleMap Class](../vs140/CSimpleMap-Class.md)   
 [CSimpleMap::FindVal](../vs140/CSimpleMap--FindVal.md)