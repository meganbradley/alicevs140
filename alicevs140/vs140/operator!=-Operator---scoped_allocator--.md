---
title: "operator!= Operator (&lt;scoped_allocator&gt;)"
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
ms.assetid: 95f2c987-8179-4ce6-92f7-b2105535f339
caps.latest.revision: 6
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator!= Operator (&lt;scoped_allocator&gt;)
Tests two `scoped_allocator_adaptor` objects for inequality.  
  
## Syntax  
  
```cpp  
template<class Outer, class... Inner>  
    bool operator!=(  
        const scoped_allocator_adaptor<Outer, Inner...>& left,  
        const scoped_allocator_adaptor<Outer, Inner...>& right) noexcept;  
```  
  
#### Parameters  
 `left`  
 The left `scoped_allocator_adaptor` object.  
  
 `right`  
 The right `scoped_allocator_adaptor` object.  
  
## Return Value  
 `!(left == right)`  
  
## Requirements  
 **Header:** <scoped_allocator>  
  
 **Namespace:** std  
  
## See Also  
 [scoped_allocator_adaptor Class](../vs140/scoped_allocator_adaptor-Class.md)   
 [operator== Operator (<scoped_allocator>)](../vs140/operator==-Operator---scoped_allocator--.md)