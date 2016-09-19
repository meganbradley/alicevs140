---
title: "false_type Typedef"
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
ms.assetid: 457e1820-b32b-4e90-a309-47b08e092819
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# false_type Typedef
Holds integral constant with false value.  
  
## Syntax  
  
```  
typedef integral_constant<bool, false> false_type;  
```  
  
## Remarks  
 The type is a synonym for a specialization of the template `integral_constant`.  
  
## Example  
  
```  
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
 [true_type](../vs140/true_type-Typedef.md)