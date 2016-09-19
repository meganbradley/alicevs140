---
title: "is_nothrow_destructible Class"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - cpp
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: language-reference
ms.assetid: 0bbd8a28-e312-4d72-bd28-aac027f974d3
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# is_nothrow_destructible Class
Tests whether the type is destructible and the destructor is known to the compiler not to throw.  
  
## Syntax  
  
```  
template <class T>  
    struct is_nothrow_destructible;  
```  
  
#### Parameters  
 `T`  
 The type to query.  
  
## Remarks  
 An instance of the type predicate holds true if the type `T` is a destructible type, and the destructor is known to the compiler not to throw. Otherwise, it holds false.  
  
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)