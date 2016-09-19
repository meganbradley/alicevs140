---
title: "operator!= Operator"
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
ms.assetid: acaa8f8e-9281-44f3-a43d-5d8a85d48f0a
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator!= Operator
Tests if the `concurrent_vector` object on the left side of the operator is not equal to the `concurrent_vector` object on the right side.  
  
## Syntax  
  
```  
template<  
   typename _Ty,  
   class A1,  
   class A2  
>  
inline bool operator!=(  
   const concurrent_vector<_Ty,  
   A1> &_A,  
   const concurrent_vector<_Ty,  
   A2> &_B  
);  
```  
  
#### Parameters  
 `_Ty`  
 The data type of the elements stored in the concurrent vectors.  
  
 `A1`  
 The allocator type of the first `concurrent_vector` object.  
  
 `A2`  
 The allocator type of the second `concurrent_vector` object.  
  
 `_A`  
 An object of type `concurrent_vector`.  
  
 `_B`  
 An object of type `concurrent_vector`.  
  
## Return Value  
 `true` if the concurrent vectors are not equal; `false` if the concurrent vectors are equal.  
  
## Remarks  
 Two concurrent vectors are equal if they have the same number of elements and their respective elements have the same values. Otherwise, they are unequal.  
  
 This method is not concurrency-safe with respect to other methods that could modify either of the concurrent vectors `_A` or `_B`.  
  
## Requirements  
 **Header:** concurrent_vector.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [concurrent_vector Class](../vs140/concurrent_vector-Class.md)   
 [Parallel Containers and Objects](../vs140/Parallel-Containers-and-Objects.md)