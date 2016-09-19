---
title: "is_nothrow_copy_assignable Class (STL)"
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
ms.assetid: 72f4dd43-e7c3-4848-af56-d4679ccb5dd7
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# is_nothrow_copy_assignable Class (STL)
Tests if type doesn't throw on assign.  
  
## Syntax  
  
```  
template<class Ty>  
    struct has_nothrow_assign;  
```  
  
#### Parameters  
 `Ty`  
 The type to query.  
  
## Remarks  
 An instance of the type predicate holds true if the type `Ty` has a nothrow copy assignment operator, otherwise it holds false.  
  
 A nothrow function is a function that has an empty throw specifier, or a function which the compiler can otherwise determine will not throw an exception.  
  
## Example  
  
```  
// std_tr1__type_traits__has_nothrow_assign.cpp   
// compile with: /EHsc   
#include <type_traits>   
#include <iostream>   
  
struct trivial   
    {   
    int val;   
    };   
  
struct throws   
    {   
    throws() throw(int)   
        {   
        }   
  
    throws(const throws&) throw(int)   
        {   
        }   
  
    throws& operator=(const throws&) throw(int)   
        {   
        }   
  
    int val;   
    };   
  
int main()   
    {   
    std::cout << "has_nothrow_assign<trivial> == " << std::boolalpha   
        << std::has_nothrow_assign<trivial>::value << std::endl;   
    std::cout << "has_nothrow_assign<throws> == " << std::boolalpha   
        << std::has_nothrow_assign<throws>::value << std::endl;   
  
    return (0);   
    }  
  
```  
  
 **has_nothrow_assign<trivial\> == true**  
**has_nothrow_assign<throws\> == false**   
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)