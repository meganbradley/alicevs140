---
title: "is_error_code_enum Class"
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
ms.assetid: cee5be2d-7c20-4cec-a352-1ab8b7d32601
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# is_error_code_enum Class
Represents a type predicate that tests for the [error_code](../vs140/error_code-Class.md) enumeration.  
  
## Syntax  
  
```  
template<_Enum>  
    class is_error_code_enum;  
```  
  
## Remarks  
 An instance of this [type predicate](../vs140/-type_traits-.md) holds true if the type `_Enum` is an enumeration value suitable for storing in an object of type `error_code`.  
  
 It is permissible to add specializations to this type for user-defined types.  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [<system_error>](../vs140/-system_error-.md)