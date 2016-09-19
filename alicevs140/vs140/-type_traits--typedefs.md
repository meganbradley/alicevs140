---
title: "&lt;type_traits&gt; typedefs"
ms.custom: na
ms.date: 09/19/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8ac040ca-ed2d-4570-adc9-cb5626530053
caps.latest.revision: 11
---
# &lt;type_traits&gt; typedefs
|||  
|-|-|  
|[false_type Typedef](#false_type_typedef)|[true_type Typedef](#true_type_typedef)|  
  
##  <a name="false_type_typedef"></a>  false_type Typedef  
 Holds integral constant with false value.  
  
```  
typedef integral_constant<bool, false> false_type;  
```  
  
### Remarks  
 The type is a synonym for a specialization of the template `integral_constant`.  
  
### Example  
  
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
##  <a name="true_type_typedef"></a>  true_type Typedef  
 Holds integral constant with true value.  
  
```  
typedef integral_constant<bool, true> true_type;  
```  
  
### Remarks  
 The type is a synonym for a specialization of the template `integral_constant`.  
  
### Example  
  
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
## See Also  
 [&lt;type_traits&gt;](../vs140/-type_traits-.md)