---
title: "concurrent_vector::crbegin Method"
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
ms.assetid: 0b4a7d9a-479d-4f8f-ad64-03f1be0320d0
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_vector::crbegin Method
Returns an iterator of type `const_reverse_iterator` to the beginning of the concurrent vector. This method is concurrency-safe.  
  
## Syntax  
  
```  
const_reverse_iterator crbegin() const;  
```  
  
## Return Value  
 An iterator of type `const_reverse_iterator` to the beginning of the concurrent vector.  
  
## Requirements  
 **Header:** concurrent_vector.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_vector Class](../vs140/concurrent_vector-Class.md)