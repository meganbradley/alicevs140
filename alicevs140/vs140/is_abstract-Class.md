---
title: "is_abstract Class"
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
ms.assetid: 8867f660-3434-404c-ba90-c26607a5e0d2
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# is_abstract Class
Tests if type is abstract class.  
  
## Syntax  
  
```  
template<class Ty>  
    struct is_abstract;  
```  
  
#### Parameters  
 `Ty`  
 The type to query.  
  
## Remarks  
 An instance of the type predicate holds true if the type `Ty` is a class that has at least one pure virtual function, otherwise it holds false.  
  
## Example  
  
```  
// std_tr1__type_traits__is_abstract.cpp   
// compile with: /EHsc   
#include <type_traits>   
#include <iostream>   
  
struct trivial   
    {   
    int val;   
    };   
  
struct abstract   
    {   
    virtual int val() = 0;   
    };   
  
int main()   
    {   
    std::cout << "is_abstract<trivial> == " << std::boolalpha   
        << std::is_abstract<trivial>::value << std::endl;   
    std::cout << "is_abstract<abstract> == " << std::boolalpha   
        << std::is_abstract<abstract>::value << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **is_abstract<trivial\> == false**  
**is_abstract<abstract\> == true**    
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [is_polymorphic](../vs140/is_polymorphic-Class.md)