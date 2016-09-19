---
title: "sync_shared::equals"
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
ms.assetid: ae1b7f02-15aa-4848-97c6-c2a3bb131e99
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# sync_shared::equals
Compares two caches for equality.  
  
## Syntax  
  
```  
bool equals(const sync_shared<Cache>& Other) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`Cache`|The type of cache associated with the synchronization filter.|  
|`Other`|The cache to compare for equality.|  
  
## Return Value  
 `true` if the result of `cache.equals(Other.cache)`, where `cache` represents the cache object, is `true`; otherwise, `false`.  
  
## Remarks  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [sync_shared Class](../vs140/sync_shared-Class.md)