---
title: "is_convertible Class"
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
ms.assetid: 75614008-1894-42ea-bd57-974399628536
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# is_convertible Class
Tests if one type is convertible to another.  
  
## Syntax  
  
```  
template<class From, class To>  
    struct is_convertible;  
```  
  
#### Parameters  
 `From`  
 The type to convert from.  
  
 `Ty`  
 The type to convert to.  
  
## Remarks  
 An instance of the type predicate holds true if the expression `To to = from;`, where `from` is an object of type `From`, is well-formed.  
  
## Example  
  
```  
// std_tr1__type_traits__is_convertible.cpp   
// compile with: /EHsc   
#include <type_traits>   
#include <iostream>   
  
struct trivial   
    {   
    int val;   
    };   
  
int main()   
    {   
    std::cout << "is_convertible<trivial, int> == " << std::boolalpha   
        << std::is_convertible<trivial, int>::value << std::endl;   
    std::cout << "is_convertible<trivial, trivial> == " << std::boolalpha   
        << std::is_convertible<trivial, trivial>::value << std::endl;   
    std::cout << "is_convertible<char, int> == " << std::boolalpha   
        << std::is_convertible<char, int>::value << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **is_convertible<trivial, int> == false**  
**is_convertible<trivial, trivial> == true**  
**is_convertible<char, int> == true**    
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [is_base_of](../vs140/is_base_of-Class.md)