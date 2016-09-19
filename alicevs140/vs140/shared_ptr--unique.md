---
title: "shared_ptr::unique"
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
ms.assetid: 13cf3869-dbb8-4d0e-854f-f5add4f1fc9a
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# shared_ptr::unique
Tests if owned resource is unique.  
  
## Syntax  
  
```  
bool unique() const;  
```  
  
## Remarks  
 The member function returns `true` if no other `shared_ptr` object owns the resource that is owned by `*this`, otherwise `false`.  
  
## Example  
  
```  
// std_tr1__memory__shared_ptr_unique.cpp   
// compile with: /EHsc   
#include <memory>   
#include <iostream>   
  
struct deleter   
    {   
    void operator()(int *p)   
        {   
        delete p;   
        }   
    };   
  
int main()   
    {   
    std::shared_ptr<int> sp1(new int(5));   
    std::cout << "sp1.unique() == " << std::boolalpha   
        << sp1.unique() << std::endl;   
  
    std::shared_ptr<int> sp2(sp1);   
    std::cout << "sp1.unique() == " << std::boolalpha   
        << sp1.unique() << std::endl;   
  
    return (0);   
    }  
  
```  
  
 **sp1.unique() == true**  
**sp1.unique() == false**   
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [shared_ptr](../vs140/shared_ptr-Class.md)