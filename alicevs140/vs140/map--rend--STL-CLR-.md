---
title: "map::rend (STL-CLR)"
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
H1: map::rend (STL/CLR)
ms.assetid: 132d9a82-f76a-4f3e-8d21-26de17e1245f
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# map::rend (STL-CLR)
Designates the end of the reversed controlled sequence.  
  
## Syntax  
  
```  
reverse_iterator rend();  
```  
  
## Remarks  
 The member function returns a reverse iterator that points just beyond the beginning of the controlled sequence. Hence, it designates the `end` of the reverse sequence. You use it to obtain an iterator that designates the `current` end of the controlled sequence seen in reverse order, but its status can change if the length of the controlled sequence changes.  
  
## Example  
  
```  
// cliext_map_rend.cpp   
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
  
// inspect first two items in reversed sequence   
    Mymap::reverse_iterator rit = c1.rend();   
    --rit;   
    --rit;   
    System::Console::WriteLine("*-- --rend() = [{0} {1}]",   
        rit->first, rit->second);   
    ++rit;   
    System::Console::WriteLine("*--rend() = [{0} {1}]",   
        rit->first, rit->second);   
    return (0);   
    }  
  
```  
  
  **[a 1] [b 2] [c 3]**  
**\*-- --rend() = [b 2]**  
**\*--rend() = [a 1]**   
## Requirements  
 **Header:** <cliext/map>  
  
 **Namespace:** cliext  
  
## See Also  
 [map](../Topic/map%20\(STL-CLR\).md)   
 [begin](../vs140/map--begin--STL-CLR-.md)   
 [end](../vs140/map--end--STL-CLR-.md)   
 [rbegin](../vs140/map--rbegin--STL-CLR-.md)