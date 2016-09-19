---
title: "is_same Class"
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
ms.assetid: d9df6c1d-c270-4ec2-802a-af275648dd1d
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# is_same Class
Tests if two types are the same.  
  
## Syntax  
  
```  
template<class Ty1, class Ty2>  
    struct is_same;  
```  
  
#### Parameters  
 `Ty1`  
 The first type to query.  
  
 `Ty2`  
 The second type to query.  
  
## Remarks  
 An instance of the type predicate holds true if the types `Ty1` and `Ty2` are the same type, otherwise it holds false.  
  
## Example  
  
```  
// std_tr1__type_traits__is_same.cpp   
// compile with: /EHsc   
#include <type_traits>   
#include <iostream>   
  
struct base   
    {   
    int val;   
    };   
  
struct derived   
    : public base   
    {   
    };   
  
int main()   
    {   
    std::cout << "is_same<base, base> == " << std::boolalpha   
        << std::is_same<base, base>::value << std::endl;   
    std::cout << "is_same<base, derived> == " << std::boolalpha   
        << std::is_same<base, derived>::value << std::endl;   
    std::cout << "is_same<derived, base> == " << std::boolalpha   
        << std::is_same<derived, base>::value << std::endl;   
    std::cout << "is_same<int, int> == " << std::boolalpha   
        << std::is_same<int, int>::value << std::endl;   
    std::cout << "is_same<int, const int> == " << std::boolalpha   
        << std::is_same<int, const int>::value << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **is_same<base, base> == true**  
**is_same<base, derived> == false**  
**is_same<derived, base> == false**  
**is_same<int, int> == true**  
**is_same<int, const int> == false**    
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [is_convertible](../vs140/is_convertible-Class.md)   
 [is_base_of](../vs140/is_base_of-Class.md)