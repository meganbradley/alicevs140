---
title: "sync_per_thread::equals"
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
ms.assetid: 0ab1054b-5a03-4009-a1f9-a87bb2f2e2b3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# sync_per_thread::equals
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
 `false` if no cache object has been allocated for this object or for `Other` in the current thread. Otherwise it returns the result of applying `operator==` to the two cache objects.  
  
## Remarks  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [sync_per_thread Class](../vs140/sync_per_thread-Class.md)