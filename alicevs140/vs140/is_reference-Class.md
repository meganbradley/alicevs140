---
title: "is_reference Class"
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
ms.assetid: 3d9e631f-3092-430c-843e-e914ab58c257
caps.latest.revision: 18
translation.priority.mt: 
  - de-de
  - ja-jp
---
# is_reference Class
Tests if type is a reference.  
  
## Syntax  
  
```  
template<class Ty>  
    struct is_reference;  
```  
  
#### Parameters  
 `Ty`  
 The type to query.  
  
## Remarks  
 An instance of the type predicate holds true if the type `Ty` is a reference to an object or to a function, otherwise it holds false.  
  
## Example  
  
```  
// std__type_traits__is_reference.cpp   
// compile with: /EHsc   
#include <type_traits>   
#include <iostream>   
  
struct trivial   
    {   
    int val;   
    };   
  
int main()   
    {   
    std::cout << "is_reference<trivial> == " << std::boolalpha   
        << std::is_reference<trivial>::value << std::endl;   
    std::cout << "is_reference<trivial&> == " << std::boolalpha   
        << std::is_reference<trivial&>::value << std::endl;   
    std::cout << "is_reference<int()> == " << std::boolalpha   
        << std::is_reference<int()>::value << std::endl;   
    std::cout << "is_reference<int(&)()> == " << std::boolalpha   
        << std::is_reference<int(&)()>::value << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **is_reference<trivial\> == false**  
**is_reference<trivial&> == true**  
**is_reference<int()> == false**  
**is_reference<int(&)()> == true**    
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [is_pointer](../vs140/is_pointer-Class.md)