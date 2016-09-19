---
title: "array::back"
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
ms.assetid: 5966939a-bdf8-42d5-bea0-b0bf68aa59c2
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# array::back
Accesses the last element.  
  
## Syntax  
  
```  
reference back();  
constexpr const_reference back() const;  
```  
  
## Remarks  
 The member functions return a reference to the last element of the controlled sequence, which must be non-empty.  
  
## Example  
  
```  
// std__array__array_back.cpp   
// compile with: /EHsc   
#include <array>   
#include <iostream>   
  
typedef std::array<int, 4> Myarray;   
int main()   
    {   
    Myarray c0 = {0, 1, 2, 3};   
  
// display contents " 0 1 2 3"   
    for (Myarray::const_iterator it = c0.begin();   
        it != c0.end(); ++it)   
        std::cout << " " << *it;   
    std::cout << std::endl;   
  
// display last element " 3"   
    std::cout << " " << c0.back();   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **0 1 2 3**  
 **3**   
## Requirements  
 **Header:** <array\>  
  
 **Namespace:** std  
  
## See Also  
 [<array\>](../vs140/-array-.md)   
 [array](../vs140/array-Class--STL-.md)   
 [front](../vs140/array--front.md)