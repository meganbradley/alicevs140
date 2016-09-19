---
title: "shared_ptr::get"
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
ms.assetid: 03a35a5e-9276-4893-ae41-d92ff3193ed9
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# shared_ptr::get
Gets address of owned resource.  
  
## Syntax  
  
```  
Ty *get() const;  
```  
  
## Remarks  
 The member function returns the address of the owned resource. If the object does not own a resource it returns 0.  
  
## Example  
  
```  
// std_tr1__memory__shared_ptr_get.cpp   
// compile with: /EHsc   
#include <memory>   
#include <iostream>   
  
int main()   
    {   
    std::shared_ptr<int> sp0;   
    std::shared_ptr<int> sp1(new int(5));   
  
    std::cout << "sp0.get() == 0 == " << std::boolalpha   
        << (sp0.get() == 0) << std::endl;   
    std::cout << "*sp1.get() == " << *sp1.get() << std::endl;   
  
    return (0);   
    }  
  
```  
  
 **sp0.get() == 0 == true**  
**\*sp1.get() == 5**   
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [shared_ptr](../vs140/shared_ptr-Class.md)   
 [shared_ptr::operator*](../vs140/shared_ptr--operator-.md)   
 [shared_ptr::operator->](../vs140/shared_ptr--operator--.md)