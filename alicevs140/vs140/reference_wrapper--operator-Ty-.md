---
title: "reference_wrapper::operator Ty&amp;"
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
ms.assetid: 9fa293c7-0a45-4e12-8ad1-72886c265690
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# reference_wrapper::operator Ty&amp;
Gets a pointer to the wrapped reference.  
  
## Syntax  
  
```  
operator Ty&() const;  
```  
  
#### Parameters  
  
## Remarks  
 The member operator returns `*ptr`.  
  
## Example  
  
```  
// std_tr1__functional__reference_wrapper_operator_cast.cpp   
// compile with: /EHsc   
#include <functional>   
#include <iostream>   
  
int main()   
    {   
    int i = 1;   
    std::reference_wrapper<int> rwi(i);   
  
    std::cout << "i = " << i << std::endl;   
    std::cout << "(int)rwi = " << (int)rwi << std::endl;   
  
    return (0);   
    }  
  
```  
  
 **i = 1**  
**(int)rwi = 1**   
## Requirements  
 **Header:** <functional\>  
  
 **Namespace:** std  
  
## See Also  
 [reference_wrapper](../vs140/reference_wrapper-Class.md)   
 [reference_wrapper::operator()](../vs140/reference_wrapper--operator--.md)