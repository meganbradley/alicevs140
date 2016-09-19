---
title: "CSimpleMap::SetAt"
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
ms.assetid: 8180d37e-3034-4867-a580-378d7c855b26
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleMap::SetAt
Sets the value associated with the given key.  
  
## Syntax  
  
```  
  
      BOOL SetAt(  
   const TKey& key,  
   const TVal& val   
);  
```  
  
#### Parameters  
 `key`  
 The key.  
  
 *val*  
 The new value to assign.  
  
## Return Value  
 Returns TRUE if the key was found, and the value was successfully changed, FALSE otherwise.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleMap Class](../vs140/CSimpleMap-Class.md)   
 [CSimpleMap::SetAtIndex](../vs140/CSimpleMap--SetAtIndex.md)