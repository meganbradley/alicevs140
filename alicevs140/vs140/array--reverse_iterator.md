---
title: "array::reverse_iterator"
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
ms.assetid: fed5a22a-6ff4-4c19-beea-1d0591abca8a
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# array::reverse_iterator
The type of a reverse iterator for the controlled sequence.  
  
## Syntax  
  
```  
typedef std::reverse_iterator<iterator> reverse_iterator;  
```  
  
## Remarks  
 The type describes an object that can serve as a reverse iterator for the controlled sequence.  
  
## Example  
  
```  
// std_tr1__array__array_reverse_iterator.cpp   
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
    Myarray::reverse_iterator it2 = c0.rbegin();   
    std::cout << " " << *it2;   
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
 [const_iterator](../vs140/array--const_iterator.md)   
 [const_reverse_iterator](../vs140/array--const_reverse_iterator.md)   
 [iterator](../vs140/array--iterator.md)