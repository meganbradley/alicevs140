---
title: "operator&lt;= (set) (STL-CLR)"
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
H1: operator&lt;= (set) (STL/CLR)
ms.assetid: acb5997b-cdc1-44d6-80c1-e20b01b4db02
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator&lt;= (set) (STL-CLR)
List less than or equal comparison.  
  
## Syntax  
  
```  
template<typename Key>  
    bool operator<=(set<Key>% left,  
        set<Key>% right);  
```  
  
#### Parameters  
 left  
 Left container to compare.  
  
 right  
 Right container to compare.  
  
## Remarks  
 The operator function returns `!(``right` `<` `left``)`. You use it to test whether `left` is not ordered after `right` when the two sets are compared element by element.  
  
## Example  
  
```  
// cliext_set_operator_le.cpp   
// compile with: /clr   
#include <cliext/set>   
  
typedef cliext::set<wchar_t> Myset;   
int main()   
    {   
    Myset c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign to a new container   
    Myset c2;   
    c2.insert(L'a');   
    c2.insert(L'b');   
    c2.insert(L'd');   
  
// display contents " a b d"   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    System::Console::WriteLine("[a b c] <= [a b c] is {0}",   
        c1 <= c1);   
    System::Console::WriteLine("[a b d] <= [a b c] is {0}",   
        c2 <= c1);   
    return (0);   
    }  
  
```  
  
  **a b c**  
 **a b d**  
**[a b c] <= [a b c] is True**  
**[a b d] <= [a b c] is False**   
## Requirements  
 **Header:** <cliext/set>  
  
 **Namespace:** cliext  
  
## See Also  
 [set](../Topic/set%20\(STL-CLR\).md)   
 [operator==](../vs140/operator==--set---STL-CLR-.md)   
 [operator!=](../vs140/operator!=--set---STL-CLR-.md)   
 [operator<](../vs140/operator---set---STL-CLR-.md)   
 [operator>=](../vs140/operator-=--set---STL-CLR-.md)   
 [operator>](../vs140/operator---set---STL-CLR-.md)