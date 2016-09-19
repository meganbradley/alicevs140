---
title: "is_nothrow_move_assignable Class"
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
ms.assetid: 000baa02-cbba-49de-9870-af730033348e
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# is_nothrow_move_assignable Class
Tests whether type has a [nothrow](../vs140/nothrow--C---.md) move assignment operator.  
  
## Syntax  
  
```  
template<class Ty>  
    struct is_nothrow_move_assignable;  
```  
  
#### Parameters  
 `Ty`  
 The type to query.  
  
## Remarks  
 An instance of the type predicate holds true if the type `Ty` has a nothrow move assignment operator, otherwise it holds false.  
  
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)