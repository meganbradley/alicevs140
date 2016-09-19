---
title: "is_trivially_move_assignable Class"
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
ms.assetid: 374f7322-0706-4bc1-a1a5-4191d0315e28
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# is_trivially_move_assignable Class
Tests whether the type has a trivial move assignment operator.  
  
## Syntax  
  
```  
template<class Ty>  
    struct is_trivially_move_assignable;  
```  
  
#### Parameters  
 `Ty`  
 The type to query.  
  
## Remarks  
 An instance of the type predicate holds true if the type `Ty` is a class that has a trivial move assignment operator, otherwise it holds false.  
  
 A move assignment operator for a class `Ty` is trivial if:  
  
 it is implicitly provided  
  
 the class `Ty` has no virtual functions  
  
 the class `Ty` has no virtual bases  
  
 the classes of all the non-static data members of class type have trivial move assignment operators  
  
 the classes of all the non-static data members of type array of class have trivial move assignment operators  
  
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)