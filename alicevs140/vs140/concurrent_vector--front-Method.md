---
title: "concurrent_vector::front Method"
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
ms.assetid: 8cd9c8b9-895c-4153-b22a-bafca902b93c
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_vector::front Method
Returns a reference or a `const` reference to the first element in the concurrent vector. If the concurrent vector is empty, the return value is undefined. This method is concurrency-safe.  
  
## Syntax  
  
```  
reference front();  
  
const_reference front() const;  
```  
  
## Return Value  
 A reference or a `const` reference to the first element in the concurrent vector.  
  
## Requirements  
 **Header:** concurrent_vector.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_vector Class](../vs140/concurrent_vector-Class.md)