---
title: "cache_suballoc::deallocate"
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
ms.assetid: 46b573ae-5d7b-4bcc-81d0-61a2f396cde8
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# cache_suballoc::deallocate
Frees a specified number of objects from storage beginning at a specified position.  
  
## Syntax  
  
```  
void deallocate(void* _Ptr, std::size_t _Count);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Ptr`|A pointer to the first object to be deallocated from storage.|  
|`_Count`|The number of objects to be deallocated from storage.|  
  
## Remarks  
  
## Requirements  
 **Header:** <allocators\>  
  
 **Namespace:** stdext  
  
## See Also  
 [cache_suballoc Class](../vs140/cache_suballoc-Class.md)