---
title: "reference_wrapper::result_type"
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
ms.assetid: a6a25311-7d85-4543-b6f5-1e99839ed96f
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# reference_wrapper::result_type
The weak result type of the wrapped reference.  
  
## Syntax  
  
```  
typedef T0 result_type;  
```  
  
## Remarks  
 The typedef is a synonym for the weak result type of a wrapped function.  
  
## Example  
  
```  
// std_tr1__functional__reference_wrapper_result_type.cpp   
// compile with: /EHsc   
#include <functional>   
#include <iostream>   
  
int neg(int val)   
    {   
    return (-val);   
    }   
  
int main()   
    {   
    typedef std::reference_wrapper<int (int)> Mywrapper;   
    Mywrapper rwi(neg);   
    Mywrapper::result_type val = rwi(3);   
  
    std::cout << "val = " << val << std::endl;   
  
    return (0);   
    }  
  
```  
  
 **val = -3**   
## Requirements  
 **Header:** <functional\>  
  
 **Namespace:** std  
  
## See Also  
 [reference_wrapper](../vs140/reference_wrapper-Class.md)   
 [reference_wrapper::operator()](../vs140/reference_wrapper--operator--.md)   
 [reference_wrapper::type](../vs140/reference_wrapper--type.md)