---
title: "sync_none::equals"
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
ms.topic: article
ms.assetid: b947f61a-f2bc-4920-88c7-ee6ee8b16568
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# sync_none::equals
Compares two caches for equality.  
  
## Syntax  
  
```  
bool equals(const sync<Cache>& Other) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`Cache`|The cache object of the synchronization filter.|  
|`Other`|The cache object to compare for equality.|  
  
## Return Value  
 The member function always returns `true`.  
  
## Remarks  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [sync_none Class](../vs140/sync_none-Class.md)