---
title: "is_lvalue_reference Class"
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
ms.assetid: 7f11896b-935c-4de1-9c87-9d0127f904e2
caps.latest.revision: 18
translation.priority.mt: 
  - de-de
  - ja-jp
---
# is_lvalue_reference Class
Tests if type is an lvalue reference.  
  
## Syntax  
  
```  
template<class Ty>  
    struct is_lvalue_reference;  
```  
  
#### Parameters  
 `Ty`  
 The type to query.  
  
## Remarks  
 An instance of this type predicate holds true if the type `Ty` is a reference to an object or to a function, otherwise it holds false. Note that `Ty` may not be an rvalue reference. For more information about rvalues, see [rvalue](../vs140/Rvalue-Reference-Declarator----.md).  
  
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [lvalues and rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)