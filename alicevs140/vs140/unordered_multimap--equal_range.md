---
title: "unordered_multimap::equal_range"
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
ms.assetid: 86007e66-5d6e-46ea-b6a2-6d6c67797d18
caps.latest.revision: 18
translation.priority.mt: 
  - de-de
  - ja-jp
---
# unordered_multimap::equal_range
Finds range that matches a specified key.  
  
## Syntax  
  
```  
std::pair<iterator, iterator>  
    equal_range(const Key& keyval);  
std::pair<const_iterator, const_iterator>  
    equal_range(const Key& keyval) const;  
```  
  
#### Parameters  
 `keyval`  
 Key value to search for.  
  
## Remarks  
 The member function returns a pair of iterators `X` such that `[X.first, X.second)` delimits just those elements of the controlled sequence that have equivalent ordering with `keyval`. If no such elements exist, both iterators are `end()`.  
  
## Example  
  
```  
// std_tr1__unordered_map__unordered_multimap_equal_range.cpp   
// compile with: /EHsc   
#include <unordered_map>   
#include <iostream>   
  
typedef std::unordered_multimap<char, int> Mymap;   
int main()   
    {   
    Mymap c1;   
  
    c1.insert(Mymap::value_type('a', 1));   
    c1.insert(Mymap::value_type('b', 2));   
    c1.insert(Mymap::value_type('c', 3));   
  
// display contents " [c 3] [b 2] [a 1]"   
    for (Mymap::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << it->first << ", " << it->second << "]";   
    std::cout << std::endl;   
  
// display results of failed search   
    std::pair<Mymap::iterator, Mymap::iterator> pair1 =   
        c1.equal_range('x');   
    std::cout << "equal_range('x'):";   
    for (; pair1.first != pair1.second; ++pair1.first)   
        std::cout << " [" << pair1.first->first   
            << ", " << pair1.first->second << "]";   
    std::cout << std::endl;   
  
// display results of successful search   
    pair1 = c1.equal_range('b');   
    std::cout << "equal_range('b'):";   
    for (; pair1.first != pair1.second; ++pair1.first)   
        std::cout << " [" << pair1.first->first   
            << ", " << pair1.first->second << "]";   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **[c, 3] [b, 2] [a, 1]**  
**equal_range('x'):**  
**equal_range('b'): [b, 2]**   
## Requirements  
 **Header:** <unordered_map>  
  
 **Namespace:** std  
  
## See Also  
 [<unordered_map>](../vs140/-unordered_map-.md)   
 [unordered_multimap](../vs140/unordered_multimap-Class.md)