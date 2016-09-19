---
title: "sync_per_container::equals"
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
ms.assetid: c370ee22-b68d-4733-ba31-eedc2d79069b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# sync_per_container::equals
Compares two caches for equality.  
  
## Syntax  
  
```  
bool equals(const sync_per_container<Cache>& Other) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`Cache`|The cache object of the synchronization filter.|  
|`Other`|The cache object to compare for equality.|  
  
## Return Value  
 The member function always returns `false`.  
  
## Remarks  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [sync_per_container Class](../vs140/sync_per_container-Class.md)