---
title: "deque::operator!= (STL-CLR)"
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
ms.topic: reference
H1: deque::operator!= (STL/CLR)
ms.assetid: c23c7bd1-813e-4518-9947-eb13d1176a13
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# deque::operator!= (STL-CLR)
Deque not equal comparison.  
  
## Syntax  
  
```  
template<typename Value>  
    bool operator!=(deque<Value>% left,  
        deque<Value>% right);  
```  
  
#### Parameters  
 left  
 Left container to compare.  
  
 right  
 Right container to compare.  
  
## Remarks  
 The operator function returns `!(``left` `==` `right``)`. You use it to test whether `left` is not ordered the same as `right` when the two deques are compared element by element.  
  
## Example  
  
```  
// cliext_deque_operator_ne.cpp   
// compile with: /clr   
#include <cliext/deque>   
  
int main()   
    {   
    cliext::deque<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign to a new container   
    cliext::deque<wchar_t> c2;   
    c2.push_back(L'a');   
    c2.push_back(L'b');   
    c2.push_back(L'd');   
  
// display contents " a b d"   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    System::Console::WriteLine("[a b c] != [a b c] is {0}",   
        c1 != c1);   
    System::Console::WriteLine("[a b c] != [a b d] is {0}",   
        c1 != c2);   
    return (0);   
    }  
  
```  
  
  **a b c**  
 **a b d**  
**[a b c] != [a b c] is False**  
**[a b c] != [a b d] is True**   
## Requirements  
 **Header:** <cliext/deque>  
  
 **Namespace:** cliext  
  
## See Also  
 [deque](../Topic/deque%20\(STL-CLR\).md)   
 [operator==](../vs140/operator==--deque---STL-CLR-.md)   
 [operator<](../vs140/operator---deque---STL-CLR-.md)   
 [operator>=](../vs140/operator-=--deque---STL-CLR-.md)   
 [operator>](../vs140/operator---deque---STL-CLR-.md)   
 [operator<=](../vs140/operator-=--deque---STL-CLR-.md)