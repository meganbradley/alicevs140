---
title: "is_nothrow_move_constructible Class"
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
ms.assetid: d186d97b-7b89-470a-8d30-993046a83379
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# is_nothrow_move_constructible Class
Tests whether type has a [nothrow](../vs140/nothrow--C---.md) move constructor.  
  
## Syntax  
  
```  
template<class Ty>  
    struct is_nothrow_move_constructible;  
```  
  
#### Parameters  
 `Ty`  
 The type to query.  
  
## Remarks  
 An instance of the type predicate holds true if the type `Ty` has a nothrow move constructor, otherwise it holds false.  
  
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)