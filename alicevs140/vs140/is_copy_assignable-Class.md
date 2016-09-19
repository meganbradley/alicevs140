---
title: "is_copy_assignable Class"
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
ms.assetid: 3ae6bca1-85fb-4829-9ee9-0183b081ff50
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# is_copy_assignable Class
Tests whether type has can be copied on assignment.  
  
## Syntax  
  
```  
template<class Ty>  
    struct is_copy_assignable;  
```  
  
#### Parameters  
 `Ty`  
 The type to query.  
  
## Remarks  
 An instance of the type predicate holds true if the type `Ty` is a class that has a copy assignment operator, otherwise it holds false. Equivalent to is_assignable<Ty&, const Ty&>.  
  
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)