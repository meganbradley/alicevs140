---
title: "weak_ptr::owner_before"
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
ms.assetid: 3f13676c-4df4-4190-8974-5116bdeae479
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# weak_ptr::owner_before
Returns `true` if this `weak_ptr` is ordered before (or less than) the provided pointer.  
  
## Syntax  
  
```  
template<class Other>  
    bool owner_before(const shared_ptr<Other>& ptr);  
template<class Other>  
    bool owner_before(const weak_ptr<Other>& ptr);  
```  
  
#### Parameters  
 `ptr`  
 An `lvalue` reference to either a `shared_ptr` or a `weak_ptr`.  
  
## Property Value/Return Value  
 Returns `true` if this `weak_ptr` sorts before the pointer parameter, `false` if not.  
  
## Remarks  
 The template member function returns `true` if `*this` is `ordered before``ptr`.  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [weak_ptr Class](../vs140/weak_ptr-Class.md)   
 [<memory\>](../vs140/-memory-.md)