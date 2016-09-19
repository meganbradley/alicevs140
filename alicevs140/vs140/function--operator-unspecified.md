---
title: "function::operator unspecified"
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
ms.assetid: d7838e8c-c932-4d29-80e0-42f227a3fe12
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# function::operator unspecified
Tests if stored callable object exists.  
  
## Syntax  
  
```  
operator unspecified();  
```  
  
## Remarks  
 The operator returns a value that is convertible to `bool` with a true value only if the object is not empty. You use it to test whether the object is empty.  
  
## Example  
  
```  
// std_tr1__functional__function_operator_bool.cpp   
// compile with: /EHsc   
#include <functional>   
#include <iostream>   
  
int neg(int val)   
    {   
    return (-val);   
    }   
  
int main()   
    {   
    std::function<int (int)> fn0;   
    std::cout << std::boolalpha << "not empty == " << (bool)fn0 << std::endl;   
  
    std::function<int (int)> fn1(neg);   
    std::cout << std::boolalpha << "not empty == " << (bool)fn1 << std::endl;   
  
    return (0);   
    }  
  
```  
  
 **not empty == false**  
**not empty == true**   
## Requirements  
 **Header:** <functional\>  
  
 **Namespace:** std  
  
## See Also  
 [function](../vs140/function-Class.md)   
 [bad_function_call](../vs140/bad_function_call-Class.md)