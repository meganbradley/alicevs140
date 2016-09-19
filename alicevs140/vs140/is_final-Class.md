---
title: "is_final Class"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - c++
ms.reviewer: na
ms.suite: na
ms.technology: 
  - cpp
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9dbad82f-6685-4909-94e8-98e4a93994b9
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# is_final Class
Tests whether the type is a class type marked `final`.  
  
## Syntax  
  
```  
template<class T>  
    struct is_final;  
```  
  
#### Parameters  
 `T`  
 The type to query.  
  
## Remarks  
 An instance of the type predicate holds true if the type `T` is a class type marked `final`, otherwise it holds false. If `T` is a class type, it must be a complete type.  
  
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [final Specifier](../vs140/final-Specifier.md)