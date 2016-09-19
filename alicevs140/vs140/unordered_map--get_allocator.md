---
title: "unordered_map::get_allocator"
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
ms.assetid: c8ad1e38-414b-4b68-a68a-21171d91395b
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# unordered_map::get_allocator
Gets the stored allocator object.  
  
## Syntax  
  
```  
Alloc get_allocator() const;  
```  
  
## Remarks  
 The member function returns the stored allocator object.  
  
## Example  
  
```  
// std_tr1__unordered_map__unordered_map_get_allocator.cpp   
// compile with: /EHsc   
#include <unordered_map>   
#include <iostream>   
  
typedef std::unordered_map<char, int> Mymap;   
typedef std::allocator<std::pair<const char, int> > Myalloc;   
int main()   
    {   
    Mymap c1;   
  
    Mymap::allocator_type al = c1.get_allocator();   
    std::cout << "al == std::allocator() is "   
        << std::boolalpha << (al == Myalloc()) << std::endl;   
  
    return (0);   
    }  
  
```  
  
 **al == std::allocator() is true**   
## Requirements  
 **Header:** <unordered_map>  
  
 **Namespace:** std  
  
## See Also  
 [<unordered_map>](../vs140/-unordered_map-.md)   
 [unordered_map](../vs140/unordered_map-Class.md)