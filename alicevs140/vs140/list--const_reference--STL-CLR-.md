---
title: "list::const_reference (STL-CLR)"
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
H1: list::const_reference (STL/CLR)
ms.assetid: bd8f6411-b8e4-4597-abd5-c0eabdf36f64
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::const_reference (STL-CLR)
The type of a constant reference to an element.  
  
## Syntax  
  
```  
typedef value_type% const_reference;  
```  
  
## Remarks  
 The type describes a constant reference to an element.  
  
## Example  
  
```  
// cliext_list_const_reference.cpp   
// compile with: /clr   
#include <cliext/list>   
  
int main()   
    {   
    cliext::list<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display initial contents " a b c"   
    cliext::list<wchar_t>::const_iterator cit = c1.begin();   
    for (; cit != c1.end(); ++cit)   
        {   // get a const reference to an element   
        cliext::list<wchar_t>::const_reference cref = *cit;   
        System::Console::Write(" {0}", cref);   
        }   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a b c**   
## Requirements  
 **Header:** <cliext/list>  
  
 **Namespace:** cliext  
  
## See Also  
 [list](../Topic/list%20\(STL-CLR\).md)   
 [reference](../vs140/list--reference--STL-CLR-.md)   
 [value_type](../vs140/list--value_type--STL-CLR-.md)