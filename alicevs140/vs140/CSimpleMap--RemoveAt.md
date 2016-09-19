---
title: "CSimpleMap::RemoveAt"
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
ms.assetid: be087e2a-a5e8-4777-8e23-59c28b6d7073
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleMap::RemoveAt
Removes a key and associated value at the specified index.  
  
## Syntax  
  
```  
  
      BOOL RemoveAt(  
   int nIndex   
);  
```  
  
#### Parameters  
 `nIndex`  
 The index of the key and associated value to remove.  
  
## Return Value  
 Returns TRUE on success, FALSE if the index specified is an invalid index.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleMap Class](../vs140/CSimpleMap-Class.md)   
 [CSimpleMap::RemoveAll](../vs140/CSimpleMap--RemoveAll.md)   
 [CSimpleMap::Remove](../vs140/CSimpleMap--Remove.md)