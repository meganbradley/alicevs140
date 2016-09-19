---
title: "true_type Typedef"
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
ms.assetid: d35de396-080d-4eb6-a695-88c662806a59
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# true_type Typedef
Holds integral constant with true value.  
  
## Syntax  
  
```  
typedef integral_constant<bool, true> true_type;  
```  
  
## Remarks  
 The type is a synonym for a specialization of the template `integral_constant`.  
  
## Example  
  
```  
// std_tr1__type_traits__true_type.cpp   
// compile with: /EHsc   
#include <type_traits>   
#include <iostream>   
  
int main()   
    {   
    std::cout << "false_type == " << std::boolalpha   
        << std::false_type::value << std::endl;   
    std::cout << "true_type == " << std::boolalpha   
        << std::true_type::value << std::endl;   
  
    return (0);   
    }  
  
```  
  
 **false_type == false**  
**true_type == true**   
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [false_type](../vs140/false_type-Typedef.md)