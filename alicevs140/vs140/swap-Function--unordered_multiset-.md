---
title: "swap Function (unordered_multiset)"
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
ms.assetid: d99cda91-6b49-4a5a-a385-c4d7d2aa57d7
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# swap Function (unordered_multiset)
Swaps the contents of two containers.  
  
## Syntax  
  
```  
template<class Key, class Hash, class Pred, class Alloc>  
    void swap(  
        unordered_multiset <Key, Hash, Pred, Alloc>& left,  
        unordered_multiset <Key, Hash, Pred, Alloc>& right);  
```  
  
#### Parameters  
 `Key`  
 The key type.  
  
 `Hash`  
 The hash function object type.  
  
 `Pred`  
 The equality comparison function object type.  
  
 `Alloc`  
 The allocator class.  
  
 `left`  
 The first container to swap.  
  
 `right`  
 The second container to swap.  
  
## Remarks  
 The template function executes `left.`[swap](../vs140/unordered_multiset--swap.md)`(right)`.  
  
## Example  
  
```  
// std_tr1__unordered_set__u_ms_swap.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
    Myset c2;   
  
    c2.insert('d');   
    c2.insert('e');   
    c2.insert('f');   
  
    c1.swap(c2);   
  
// display contents " [f] [e] [d]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
    swap(c1, c2);   
  
// display contents " [c] [b] [a]"   
    for (Myset::const_iterator it = c1.begin();   
        it != c1.end(); ++it)   
        std::cout << " [" << *it << "]";   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **[c] [b] [a]**  
 **[f] [e] [d]**  
 **[c] [b] [a]**   
## Requirements  
 **Header:** <unordered_set>  
  
 **Namespace:** std  
  
## See Also  
 [<unordered_set>](../vs140/-unordered_set-.md)   
 [swap](../vs140/unordered_multiset--swap.md)