---
title: "concurrent_vector::operatorOperator"
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
ms.assetid: 1875880f-643b-4d60-ab59-a27f480313e5
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_vector::operatorOperator
Provides access to the element at the given index in the concurrent vector. This method is concurrency-safe for read operations, and also while growing the vector, as long as the you have ensured that the value `_Index` is less than the size of the concurrent vector.  
  
## Syntax  
  
```  
reference operator[](size_type _Index);  
  
const_reference operator[](size_type _Index) const;  
```  
  
#### Parameters  
 `_Index`  
 The index of the element to be retrieved.  
  
## Return Value  
 A reference to the item at the given index.  
  
## Remarks  
 The version of `operator []` that returns a non-`const` reference cannot be used to concurrently write to the element from different threads. A different synchronization object should be used to synchronize concurrent read and write operations to the same data element.  
  
 No bounds checking is performed to ensure that `_Index` is a valid index into the concurrent vector.  
  
## Requirements  
 **Header:** concurrent_vector.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_vector Class](../vs140/concurrent_vector-Class.md)