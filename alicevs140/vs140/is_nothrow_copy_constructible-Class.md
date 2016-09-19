---
title: "is_nothrow_copy_constructible Class"
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
ms.assetid: f13a0bea-63b1-492a-9a45-d445df35c282
caps.latest.revision: 22
translation.priority.mt: 
  - de-de
  - ja-jp
---
# is_nothrow_copy_constructible Class
Tests whether type has a [nothrow](../vs140/nothrow--C---.md) copy constructor.  
  
## Syntax  
  
```  
template<class Ty>  
    struct is_nothrow_copy_constructible;  
```  
  
#### Parameters  
 `Ty`  
 The type to query.  
  
## Remarks  
 An instance of the type predicate holds true if the type `Ty` has a nothrow copy constructor, otherwise it holds false.  
  
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)