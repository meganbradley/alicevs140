---
title: "unordered_map::hasher"
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
ms.assetid: 646fd827-accd-4449-9ea9-fad4cf2bb488
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# unordered_map::hasher
The type of the hash function.  
  
## Syntax  
  
```  
typedef Hash hasher;  
```  
  
## Remarks  
 The type is a synonym for the template parameter `Hash`.  
  
## Example  
  
```  
// std_tr1__unordered_map__unordered_map_hasher.cpp   
// compile with: /EHsc   
#include <unordered_map>   
#include <iostream>   
  
typedef std::unordered_map<char, int> Mymap;   
int main()   
    {   
    Mymap c1;   
  
    Mymap::hasher hfn = c1.hash_function();   
    std::cout << "hfn('a') == " << hfn('a') << std::endl;   
    std::cout << "hfn('b') == " << hfn('b') << std::endl;   
  
    return (0);   
    }  
  
```  
  
 **hfn('a') == 1630279**  
**hfn('b') == 1647086**   
## Requirements  
 **Header:** <unordered_map>  
  
 **Namespace:** std  
  
## See Also  
 [<unordered_map>](../vs140/-unordered_map-.md)   
 [unordered_map](../vs140/unordered_map-Class.md)