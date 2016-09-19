---
title: "map::operator(STL-CLR)"
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
H1: map::operator(STL/CLR)
ms.assetid: 50e494c5-62d4-4469-8da3-7432ee4dff97
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# map::operator(STL-CLR)
Maps a key to its associated mapped value.  
  
## Syntax  
  
```  
mapped_type operator[](key_type key);  
```  
  
#### Parameters  
 key  
 Key value to search for.  
  
## Remarks  
 The member functions endeavors to find an element with equivalent ordering to `key`. If it finds one, it returns the associated mapped value; otherwise, it inserts `value_type(``key``, mapped_type())` and returns the associated (default) mapped value. You use it to look up a mapped value given its associated key, or to ensure that an entry exists for the key if none is found.  
  
## Example  
  
```  
// cliext_map_operator_sub.cpp   
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
  
    System::Console::WriteLine("c1[{0}] = {1}",   
        L'A', c1[L'A']);   
    System::Console::WriteLine("c1[{0}] = {1}",   
        L'b', c1[L'b']);   
  
// redisplay altered contents   
    for each (Mymap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// alter mapped values and redisplay   
    c1[L'A'] = 10;   
    c1[L'c'] = 13;   
    for each (Mymap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **[a 1] [b 2] [c 3]**  
**c1[A] = 0**  
**c1[b] = 2**  
 **[A 0] [a 1] [b 2] [c 3]**  
 **[A 10] [a 1] [b 2] [c 13]**   
## Requirements  
 **Header:** <cliext/map>  
  
 **Namespace:** cliext  
  
## See Also  
 [map](../Topic/map%20\(STL-CLR\).md)   
 [find](../vs140/map--find--STL-CLR-.md)   
 [insert](../vs140/map--insert--STL-CLR-.md)