---
title: "multimap::to_array (STL-CLR)"
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
H1: multimap::to_array (STL/CLR)
ms.assetid: eb4872dd-5e32-4a82-8ad4-37b533eb6814
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multimap::to_array (STL-CLR)
Copies the controlled sequence to a new array.  
  
## Syntax  
  
```  
cli::array<value_type>^ to_array();  
```  
  
## Remarks  
 The member function returns an array containing the controlled sequence. You use it to obtain a copy of the controlled sequence in array form.  
  
## Example  
  
```  
// cliext_multimap_to_array.cpp   
// compile with: /clr   
#include <cliext/map>   
  
typedef cliext::multimap<wchar_t, int> Mymultimap;   
int main()   
    {   
    Mymultimap c1;   
    c1.insert(Mymultimap::make_value(L'a', 1));   
    c1.insert(Mymultimap::make_value(L'b', 2));   
    c1.insert(Mymultimap::make_value(L'c', 3));   
  
// copy the container and modify it   
    cli::array<Mymultimap::value_type>^ a1 = c1.to_array();   
  
    c1.insert(Mymultimap::make_value(L'd', 4));   
    for each (Mymultimap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// display the earlier array copy   
    for each (Mymultimap::value_type elem in a1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **[a 1] [b 2] [c 3] [d 4]**  
 **[a 1] [b 2] [c 3]**   
## Requirements  
 **Header:** <cliext/map>  
  
 **Namespace:** cliext  
  
## See Also  
 [multimap](../Topic/multimap%20\(STL-CLR\).md)