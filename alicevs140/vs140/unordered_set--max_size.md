---
title: "unordered_set::max_size"
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
ms.assetid: 0f28935e-f33a-495d-a130-3a885cdf8af5
caps.latest.revision: 18
translation.priority.mt: 
  - de-de
  - ja-jp
---
# unordered_set::max_size
Gets the maximum size of the controlled sequence.  
  
## Syntax  
  
```  
size_type max_size() const;  
```  
  
## Remarks  
 The member function returns the length of the longest sequence that the object can control.  
  
## Example  
  
```  
// std_tr1__unordered_set__unordered_set_max_size.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_set<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    std::cout << "max_size() == " << c1.max_size() << std::endl;   
  
    return (0);   
    }  
  
```  
  
 **max_size() == 4294967295**   
## Requirements  
 **Header:** <unordered_set>  
  
 **Namespace:** std  
  
## See Also  
 [<unordered_set>](../vs140/-unordered_set-.md)   
 [unordered_set](../vs140/unordered_set-Class.md)   
 [unordered_set::size](../vs140/unordered_set--size.md)