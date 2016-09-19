---
title: "Free Function"
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
ms.assetid: cde873ad-874b-482d-aae3-451f2e380d2b
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Free Function
Releases a block of memory previously allocated by the `Alloc` method to the Concurrency Runtime Caching Suballocator.  
  
## Syntax  
  
```  
void __cdecl Free(  
   _Pre_maybenull_ _Post_invalid_ void * _PAllocation  
);  
```  
  
#### Parameters  
 `_PAllocation`  
 A pointer to memory previously allocated by the `Alloc` method which is to be freed. If the parameter `_PAllocation` is set to the value `NULL`, this method will ignore it and return immediately.  
  
## Remarks  
 For more information about which scenarios in your application could benefit from using the Caching Suballocator, see [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md).  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [Concurrency::Alloc Function](assetId:///f91f155a-20af-477e-baa2-e49a0437ff08)