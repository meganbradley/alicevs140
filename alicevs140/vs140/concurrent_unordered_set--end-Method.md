---
title: "concurrent_unordered_set::end Method"
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
ms.assetid: 19d1e2a8-4b7d-4391-9483-193a813eb02b
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_unordered_set::end Method
Returns an iterator pointing to the location succeeding the last element in the concurrent container. This method is concurrency safe.  
  
## Syntax  
  
```  
iterator end();  
  
const_iterator end() const;  
```  
  
## Return Value  
 An iterator to the location succeeding the last element in the concurrent container.  
  
## Requirements  
 **Header:** internal_concurrent_hash.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_unordered_set Class](../vs140/concurrent_unordered_set-Class.md)