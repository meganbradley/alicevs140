---
title: "shared_ptr::owner_before"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2519274c-b9ad-42e2-9b4e-ddacaeee4946
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# shared_ptr::owner_before
Returns true if this `shared_ptr` is ordered before (or less than) the provided pointer.  
  
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
 Returns true if this `shared_ptr` sorts before the pointer parameter, false if not.  
  
## Remarks  
 The template member function returns true if `*this` is `ordered before``ptr`.  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [owner_before](../vs140/shared_ptr--owner_before.md)