---
title: "swap Function"
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
ms.assetid: 1d6508df-4435-4acf-9fe6-eaa70c5dfd17
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# swap Function
Exchanges the elements of two `concurrent_vector` objects.  
  
## Syntax  
  
```  
template<  
   typename _Ty,  
   class _Ax  
>  
inline void swap(  
   concurrent_vector<_Ty,  
   _Ax> &_A,  
   concurrent_vector<_Ty,  
   _Ax> &_B  
);  
```  
  
#### Parameters  
 `_Ty`  
 The data type of the elements stored in the concurrent vectors.  
  
 `_Ax`  
 The allocator type of the concurrent vectors.  
  
 `_A`  
 The concurrent vector whose elements are to be exchanged with those of the concurrent vector `_B`.  
  
 `_B`  
 The concurrent vector providing the elements to be swapped, or the vector whose elements are to be exchanged with those of the concurrent vector `_A`.  
  
## Remarks  
 The template function is an algorithm specialized on the container class `concurrent_vector` to execute the member function `_A`.[concurrent_vector::swap](../vs140/concurrent_vector--swap-Method.md)(`_B`). These are instances of the partial ordering of function templates by the compiler. When template functions are overloaded in such a way that the match of the template with the function call is not unique, then the compiler will select the most specialized version of the template function. The general version of the template function, `template <class T> void swap(T&, T&)`, in the algorithm class works by assignment and is a slow operation. The specialized version in each container is much faster as it can work with the internal representation of the container class.  
  
 This method is not concurrency-safe. You must ensure that no other threads are performing operations on either of the concurrent vectors when you call this method.  
  
## Requirements  
 **Header:** concurrent_vector.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [concurrent_vector Class](../vs140/concurrent_vector-Class.md)   
 [Parallel Containers and Objects](../vs140/Parallel-Containers-and-Objects.md)