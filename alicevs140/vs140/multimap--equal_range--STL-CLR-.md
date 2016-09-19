---
title: "multimap::equal_range (STL-CLR)"
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
H1: multimap::equal_range (STL/CLR)
ms.assetid: f1008d89-7442-429b-9eca-4ef7ee704766
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multimap::equal_range (STL-CLR)
Finds range that matches a specified key.  
  
## Syntax  
  
```  
pair_iter_iter equal_range(key_type _Keyval);  
```  
  
#### Parameters  
 `_Keyval`  
 Key value to search for.  
  
## Remarks  
 The method returns a pair of iterators `-` [lower_bound](../vs140/multimap--lower_bound--STL-CLR-.md)`(``_Keyval``),` [upper_bound](../vs140/multimap--upper_bound--STL-CLR-.md)`(``_Keyval``)`. You use it to determine the range of elements currently in the controlled sequence that match a specified key.  
  
## Example  
  
```  
// cliext_multimap_equal_range.cpp   
// compile with: /clr   
#include <cliext/map>   
  
typedef cliext::multimap<wchar_t, int> Mymultimap;   
typedef Mymultimap::pair_iter_iter Pairii;   
int main()   
    {   
    Mymultimap c1;   
    c1.insert(Mymultimap::make_value(L'a', 1));   
    c1.insert(Mymultimap::make_value(L'b', 2));   
    c1.insert(Mymultimap::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Mymultimap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// display results of failed search   
    Pairii pair1 = c1.equal_range(L'x');   
    System::Console::WriteLine("equal_range(L'x') empty = {0}",   
        pair1.first == pair1.second);   
  
// display results of successful search   
    pair1 = c1.equal_range(L'b');   
    for (; pair1.first != pair1.second; ++pair1.first)   
        System::Console::Write(" [{0} {1}]",   
            pair1.first->first, pair1.first->second);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **[a 1] [b 2] [c 3]**  
**equal_range(L'x') empty = True**  
 **[b 2]**   
## Requirements  
 **Header:** <cliext/map>  
  
 **Namespace:** cliext  
  
## See Also  
 [multimap](../Topic/multimap%20\(STL-CLR\).md)   
 [count](../vs140/multimap--count--STL-CLR-.md)   
 [find](../vs140/multimap--find--STL-CLR-.md)   
 [lower_bound](../vs140/multimap--lower_bound--STL-CLR-.md)   
 [upper_bound](../vs140/multimap--upper_bound--STL-CLR-.md)