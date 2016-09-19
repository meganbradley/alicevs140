---
title: "combinable::combinable Constructor"
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
ms.assetid: c24b9603-90ea-4cb2-8cb8-13d5b9c17887
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# combinable::combinable Constructor
Constructs a new `combinable` object.  
  
## Syntax  
  
```  
combinable();  
  
template <  
   typename _Function  
>  
explicit combinable(  
   _Function_FnInitialize  
);  
  
combinable(  
   const combinable& _Copy  
);  
```  
  
#### Parameters  
 `_Function`  
 The type of the initialization functor object.  
  
 `_FnInitialize`  
 A function which will be called to initialize each new thread-private value of the type `_Ty`. It must support a function call operator with the signature `_Ty ()`.  
  
 `_Copy`  
 An existing `combinable` object to be copied into this one.  
  
## Remarks  
 The first constructor initializes new elements with the default constructor for the type `_Ty`.  
  
 The second constructor initializes new elements using the initialization functor supplied as the `_FnInitialize` parameter.  
  
 The third constructor is the copy constructor.  
  
## Requirements  
 **Header:** ppl.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [combinable Class](../vs140/combinable-Class.md)   
 [Parallel Containers and Objects](../vs140/Parallel-Containers-and-Objects.md)