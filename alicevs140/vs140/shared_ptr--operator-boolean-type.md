---
title: "shared_ptr::operator boolean-type"
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
ms.assetid: d206b994-37bd-4e10-a7ee-7019340cfe8a
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# shared_ptr::operator boolean-type
Tests if an owned resource exists.  
  
## Syntax  
  
```  
operator boolean-type() const;  
```  
  
## Remarks  
 The operator returns a value of a type that is convertible to `bool`. The result of the conversion to `bool` is `true` when `get() != 0`, otherwise `false`.  
  
## Example  
  
```  
// std_tr1__memory__shared_ptr_operator_bool.cpp   
// compile with: /EHsc   
#include <memory>   
#include <iostream>   
  
int main()   
    {   
    std::shared_ptr<int> sp0;   
    std::shared_ptr<int> sp1(new int(5));   
  
    std::cout << "(bool)sp0 == " << std::boolalpha   
        << (bool)sp0 << std::endl;   
    std::cout << "(bool)sp1 == " << std::boolalpha   
        << (bool)sp1 << std::endl;   
  
    return (0);   
    }  
  
```  
  
 **(bool)sp0 == false**  
**(bool)sp1 == true**   
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [shared_ptr](../vs140/shared_ptr-Class.md)   
 [shared_ptr::get](../vs140/shared_ptr--get.md)