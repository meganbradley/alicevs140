---
title: "CSimpleMap::GetKeyAt"
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
ms.assetid: 1c958fd6-87cf-42e6-b093-6264c27d460a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleMap::GetKeyAt
Retrieves the key at the specified index.  
  
## Syntax  
  
```  
  
      TKey& GetKeyAt(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 The index of the key to return.  
  
## Return Value  
 Returns the key referenced by `nIndex`.  
  
## Remarks  
 The index passed by `nIndex` must be valid for the return value to be meaningful.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleMap Class](../vs140/CSimpleMap-Class.md)   
 [CSimpleMap::GetValueAt](../vs140/CSimpleMap--GetValueAt.md)