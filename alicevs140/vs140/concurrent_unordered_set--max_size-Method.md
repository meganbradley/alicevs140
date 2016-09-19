---
title: "concurrent_unordered_set::max_size Method"
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
ms.assetid: 2ed26a81-b7eb-46f0-8453-0c5e7cf33f4e
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_unordered_set::max_size Method
Returns the maximum size of the concurrent container, determined by the allocator. This method is concurrency safe.  
  
## Syntax  
  
```  
size_type max_size() const;  
```  
  
## Return Value  
 The maximum number of elements that can be inserted into this concurrent container.  
  
## Remarks  
 This upper bound value may actually be higher than what the container can actually hold.  
  
## Requirements  
 **Header:** internal_concurrent_hash.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_unordered_set Class](../vs140/concurrent_unordered_set-Class.md)