---
title: "is_trivially_copy_assignable Class"
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
ms.assetid: 7410133e-f367-493f-92a7-e34e3ec5e879
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# is_trivially_copy_assignable Class
Tests whether the type has a trivial copy assignment operator.  
  
## Syntax  
  
```  
template<class Ty>  
    struct is_trivially_copy_assignable;  
```  
  
#### Parameters  
 `T`  
 The type to query.  
  
## Remarks  
 An instance of the type predicate holds true if the type `T` is a class that has a trivial copy assignment operator, otherwise it holds false.  
  
 An assignment constructor for a class `T` is trivial if it is implicitly provided, the class `T` has no virtual functions, the class `T` has no virtual bases, the classes of all the non-static data members of class type have trivial assignment operators, and the classes of all the non-static data members of type array of class have trivial assignment operators.  
  
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)