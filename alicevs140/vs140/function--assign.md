---
title: "function::assign"
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
ms.assetid: ae6afc85-a7e1-4246-b130-af075b9720c5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# function::assign
Assigns a callable object to this function object.  
  
## Syntax  
  
```  
template<class Fx, class Alloc>  
    void assign(  
        Fx _Func,   
        const Alloc& _Ax  
);  
template<class Fx, class Alloc>  
    void assign(  
        reference_wrapper<Fx> _Fnref,   
        const Alloc& _Ax  
);  
```  
  
#### Parameters  
 `_Func`  
 A callable object.  
  
 `_Fnref`  
 A reference wrapper that contains a callable object.  
  
 `_Ax`  
 An allocator object.  
  
## Property Value/Return Value  
  
## Remarks  
 The member functions each replace the `callable object` held by `*this` with the callable object passed as the `operand`. Both allocate storage with the allocator object `_Ax`.  
  
## Requirements  
 **Header:** <functional\>  
  
 **Namespace:** std  
  
## See Also  
 [function](../vs140/function-Class.md)   
 [mem_fn](../vs140/mem_fn-Function.md)   
 [lvalues and rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)   
 [reference_wrapper](../vs140/reference_wrapper-Class.md)