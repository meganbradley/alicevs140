---
title: "combinable::combine Method"
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
ms.assetid: 492e55cc-c1f8-4e0e-8356-2636f25563de
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# combinable::combine Method
Computes a final value from the set of thread-local sub-computations by calling the supplied combine functor.  
  
## Syntax  
  
```  
template<  
   typename _Function  
>  
_Ty combine(  
   _Function_FnCombine  
) const;  
```  
  
#### Parameters  
 `_Function`  
 The type of the function object that will be invoked to combine two thread-local sub-computations.  
  
 `_FnCombine`  
 The functor that is used to combine the sub-computations. Its signature is `T (T, T)` or `T (const T&, const T&)`, and it must be associative and commutative.  
  
## Return Value  
 The final result of combining all the thread-private sub-computations.  
  
## Requirements  
 **Header:** ppl.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [combinable Class](../vs140/combinable-Class.md)   
 [Parallel Containers and Objects](../vs140/Parallel-Containers-and-Objects.md)