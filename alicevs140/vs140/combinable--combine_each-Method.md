---
title: "combinable::combine_each Method"
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
ms.assetid: ac44fbc7-69b5-44dc-86f8-b772dab6729b
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# combinable::combine_each Method
Computes a final value from the set of thread-local sub-computations by calling the supplied combine functor once per thread-local sub-computation. The final result is accumulated by the function object.  
  
## Syntax  
  
```  
template<  
   typename _Function  
>  
void combine_each(  
   _Function_FnCombine  
) const;  
```  
  
#### Parameters  
 `_Function`  
 The type of the function object that will be invoked to combine a single thread-local sub-computation.  
  
 `_FnCombine`  
 The functor that is used to combine one sub-computation. Its signature is `void (T)` or `void (const T&)`, and must be associative and commutative.  
  
## Requirements  
 **Header:** ppl.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [combinable Class](../vs140/combinable-Class.md)   
 [Parallel Containers and Objects](../vs140/Parallel-Containers-and-Objects.md)