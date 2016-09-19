---
title: "reference_wrapper::type"
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
ms.assetid: d39d0b04-417b-45db-be4f-32f4c1f25504
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# reference_wrapper::type
The type of the wrapped reference.  
  
## Syntax  
  
```  
typedef Ty type;  
```  
  
## Remarks  
 The typedef is a synonym for the template argument `Ty`.  
  
## Example  
  
```  
// std_tr1__functional__reference_wrapper_type.cpp   
// compile with: /EHsc   
#include <functional>   
#include <iostream>   
  
int neg(int val)   
    {   
    return (-val);   
    }   
  
int main()   
    {   
    int i = 1;   
    typedef std::reference_wrapper<int> Mywrapper;   
    Mywrapper rwi(i);   
    Mywrapper::type val = rwi.get();   
  
    std::cout << "i = " << i << std::endl;   
    std::cout << "rwi = " << val << std::endl;   
  
    return (0);   
    }  
  
```  
  
 **i = 1**  
**rwi = 1**   
## Requirements  
 **Header:** <functional\>  
  
 **Namespace:** std  
  
## See Also  
 [reference_wrapper](../vs140/reference_wrapper-Class.md)   
 [reference_wrapper::result_type](../vs140/reference_wrapper--result_type.md)