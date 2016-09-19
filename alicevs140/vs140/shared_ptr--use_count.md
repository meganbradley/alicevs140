---
title: "shared_ptr::use_count"
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
ms.assetid: 5250d0a0-de32-4b0c-a5fc-49a13500d4c8
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# shared_ptr::use_count
Counts numbers of resource owners.  
  
## Syntax  
  
```  
long use_count() const;  
```  
  
## Remarks  
 The member function returns the number of `shared_ptr` objects that own the resource that is owned by `*this`.  
  
## Example  
  
```  
// std_tr1__memory__shared_ptr_use_count.cpp   
// compile with: /EHsc   
#include <memory>   
#include <iostream>   
  
int main()   
    {   
    std::shared_ptr<int> sp1(new int(5));   
    std::cout << "sp1.use_count() == "   
        << sp1.use_count() << std::endl;   
  
    std::shared_ptr<int> sp2(sp1);   
    std::cout << "sp1.use_count() == "   
        << sp1.use_count() << std::endl;   
  
    return (0);   
    }  
  
```  
  
 **sp1.use_count() == 1**  
**sp1.use_count() == 2**   
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [shared_ptr](../vs140/shared_ptr-Class.md)