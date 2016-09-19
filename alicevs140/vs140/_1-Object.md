---
title: "_1 Object"
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
ms.assetid: 30c3c480-ff31-4708-94be-7d0d65f243c9
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _1 Object
Placeholders for replaceable arguments.  
  
## Syntax  
  
```  
namespace placeholders {  
  extern             unspecified _1, _2, ... _M  
  } // namespace placeholders (within std)  
```  
  
## Remarks  
 The objects `_1, _2, ... _M` are placeholders designating the first, second, ..., Mth argument, respectively in a function call to an object returned by [bind](../vs140/-functional--functions.md#bind_function). You use `_N` to specify where the Nth argument should be inserted when the bind expression is evaluated.  
  
 In this implementation the value of `M` is 20.  
  
## Example  
  
```cpp  
// std__functional_placeholder.cpp   
// compile with: /EHsc   
#include <functional>   
#include <algorithm>   
#include <iostream>   
  
using namespace std::placeholders;   
  
void square(double x)   
    {   
    std::cout << x << "^2 == " << x * x << std::endl;   
    }   
  
void product(double x, double y)   
    {   
    std::cout << x << "*" << y << " == " << x * y << std::endl;   
    }   
  
int main()   
    {   
    double arg[] = {1, 2, 3};   
  
    std::for_each(&arg[0], &arg[3], square);   
    std::cout << std::endl;   
  
    std::for_each(&arg[0], &arg[3], std::bind(product, _1, 2));   
    std::cout << std::endl;   
  
    std::for_each(&arg[0], &arg[3], std::bind(square, _1));   
  
    return (0);   
    }  
  
```  
  
  **1^2 == 1**  
**2^2 == 4**  
**3^2 == 9**  
**1\*2 == 2**  
**2\*2 == 4**  
**3\*2 == 6**  
**1^2 == 1**  
**2^2 == 4**  
**3^2 == 9**    
## Requirements  
 **Header:** <functional\>  
  
 **Namespace:** std  
  
## See Also  
 [bind](../vs140/-functional--functions.md#bind_function)   
 [is_placeholder](../vs140/is_placeholder-Class.md)