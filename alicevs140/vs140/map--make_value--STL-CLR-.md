---
title: "map::make_value (STL-CLR)"
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
H1: map::make_value (STL/CLR)
ms.assetid: a0bc4081-b8b7-450e-b041-a49ac42b279f
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# map::make_value (STL-CLR)
Constructs a value object.  
  
## Syntax  
  
```  
static value_type make_value(key_type key, mapped_type mapped);  
```  
  
#### Parameters  
 key  
 Key value to use.  
  
 mapped  
 Mapped value to search for.  
  
## Remarks  
 The member function returns a `value_type` object whose key is `key` and whose mapped value is `mapped`. You use it to compose an object suitable for use with several other member functions.  
  
## Example  
  
```  
// cliext_map_make_value.cpp   
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
    return (0);   
    }  
  
```  
  
  **[a 1] [b 2] [c 3]**   
## Requirements  
 **Header:** <cliext/map>  
  
 **Namespace:** cliext  
  
## See Also  
 [map](../Topic/map%20\(STL-CLR\).md)   
 [key_type](../vs140/map--key_type--STL-CLR-.md)   
 [mapped_type](../vs140/map--mapped_type--STL-CLR-.md)   
 [value_type](../vs140/map--value_type--STL-CLR-.md)