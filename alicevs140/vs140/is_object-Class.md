---
title: "is_object Class"
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
ms.assetid: b452ceea-5676-488f-925b-ab881126c387
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# is_object Class
Tests if type is an object type.  
  
## Syntax  
  
```  
template<class Ty>  
    struct is_object;  
```  
  
#### Parameters  
 `Ty`  
 The type to query.  
  
## Remarks  
 An instance of the type predicate holds false if the type `Ty` is a reference type, a function type, or void, or a `cv-qualified` form of one of them, otherwise holds true.  
  
## Example  
  
```  
// std_tr1__type_traits__is_object.cpp   
// compile with: /EHsc   
#include <type_traits>   
#include <iostream>   
  
struct trivial   
    {   
    int val;   
    };   
  
struct functional   
    {   
    int f();   
    };   
  
int main()   
    {   
    std::cout << "is_object<trivial> == " << std::boolalpha   
        << std::is_object<trivial>::value << std::endl;   
    std::cout << "is_object<functional> == " << std::boolalpha   
        << std::is_object<functional>::value << std::endl;   
    std::cout << "is_object<trivial&> == " << std::boolalpha   
        << std::is_object<trivial&>::value << std::endl;   
    std::cout << "is_object<float()> == " << std::boolalpha   
        << std::is_object<float()>::value << std::endl;   
    std::cout << "is_object<void> == " << std::boolalpha   
        << std::is_object<void>::value << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **is_object<trivial\> == true**  
**is_object<functional\> == true**  
**is_object<trivial&> == false**  
**is_object<float()> == false**  
**is_object<void\> == false**    
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [is_function](../vs140/is_function-Class.md)