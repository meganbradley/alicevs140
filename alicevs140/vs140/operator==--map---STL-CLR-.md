---
title: "operator== (map) (STL-CLR)"
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
H1: operator== (map) (STL/CLR)
ms.assetid: 6f7672af-71f8-4086-ac42-173203e52951
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator== (map) (STL-CLR)
List equal comparison.  
  
## Syntax  
  
```  
template<typename Key,  
    typename Mapped>  
    bool operator==(map<Key, Mapped>% left,  
        map<Key, Mapped>% right);  
```  
  
#### Parameters  
 left  
 Left container to compare.  
  
 right  
 Right container to compare.  
  
## Remarks  
 The operator function returns true only if the sequences controlled by `left` and `right` have the same length and, for each position `i`, `left``[i] ==` `right``[i]`. You use it to test whether `left` is ordered the same as `right` when the two maps are compared element by element.  
  
## Example  
  
```  
// cliext_map_operator_eq.cpp   
// compile with: /clr   
#include <cliext/map>   
  
typedef cliext::map<wchar_t, int> Mymap;   
int main()   
    {   
    Mymap c1;   
    c1.insert(Mymap::make_value(L'a', 1));   
    c1.insert(Mymap::make_value(L'b', 2));   
    c1.insert(Mymap::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Mymap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// assign to a new container   
    Mymap c2;   
    c2.insert(Mymap::make_value(L'a', 1));   
    c2.insert(Mymap::make_value(L'b', 2));   
    c2.insert(Mymap::make_value(L'd', 4));   
  
// display contents " [a 1] [b 2] [d 4]"   
    for each (Mymap::value_type elem in c2)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
    System::Console::WriteLine("[a b c] == [a b c] is {0}",   
        c1 == c1);   
    System::Console::WriteLine("[a b c] == [a b d] is {0}",   
        c1 == c2);   
    return (0);   
    }  
  
```  
  
  **[a 1] [b 2] [c 3]**  
 **[a 1] [b 2] [d 4]**  
**[a b c] == [a b c] is True**  
**[a b c] == [a b d] is False**   
## Requirements  
 **Header:** <cliext/map>  
  
 **Namespace:** cliext  
  
## See Also  
 [map](../Topic/map%20\(STL-CLR\).md)   
 [operator!=](../vs140/operator!=--map---STL-CLR-.md)   
 [operator<](../vs140/operator---map---STL-CLR-.md)   
 [operator>=](../vs140/operator-=--map---STL-CLR-.md)   
 [operator>](../vs140/operator---map---STL-CLR-.md)   
 [operator<=](../vs140/operator-=--map---STL-CLR-.md)