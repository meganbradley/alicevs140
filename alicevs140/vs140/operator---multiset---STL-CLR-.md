---
title: "operator&lt; (multiset) (STL-CLR)"
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
H1: operator&lt; (multiset) (STL/CLR)
ms.assetid: 48150cda-4f3e-4535-860c-89f622a7f0a8
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator&lt; (multiset) (STL-CLR)
List less than comparison.  
  
## Syntax  
  
```  
template<typename Key>  
    bool operator<(multiset<Key>% left,  
        multiset<Key>% right);  
```  
  
#### Parameters  
 left  
 Left container to compare.  
  
 right  
 Right container to compare.  
  
## Remarks  
 The operator function returns true if, for the lowest position `i` for which `!(``right``[i] <` `left``[i])` it is also true that `left``[i] <` `right``[i]`. Otherwise, it returns `left``->size() <` `right``->size()` You use it to test whether `left` is ordered before `right` when the two multisets are compared element by element.  
  
## Example  
  
```  
// cliext_multiset_operator_lt.cpp   
// compile with: /clr   
#include <cliext/set>   
  
typedef cliext::multiset<wchar_t> Mymultiset;   
int main()   
    {   
    Mymultiset c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign to a new container   
    Mymultiset c2;   
    c2.insert(L'a');   
    c2.insert(L'b');   
    c2.insert(L'd');   
  
// display contents " a b d"   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    System::Console::WriteLine("[a b c] < [a b c] is {0}",   
        c1 < c1);   
    System::Console::WriteLine("[a b c] < [a b d] is {0}",   
        c1 < c2);   
    return (0);   
    }  
  
```  
  
  **a b c**  
 **a b d**  
**[a b c] < [a b c] is False**  
**[a b c] < [a b d] is True**   
## Requirements  
 **Header:** <cliext/set>  
  
 **Namespace:** cliext  
  
## See Also  
 [multiset](../Topic/multiset%20\(STL-CLR\).md)   
 [operator==](../vs140/operator==--multiset---STL-CLR-.md)   
 [operator!=](../vs140/operator!=--multiset---STL-CLR-.md)   
 [operator>=](../vs140/operator-=--multiset---STL-CLR-.md)   
 [operator>](../vs140/operator---multiset---STL-CLR-.md)   
 [operator<=](../vs140/operator-=--multiset---STL-CLR-.md)