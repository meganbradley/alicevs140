---
title: "multiset::reference (STL-CLR)"
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
H1: multiset::reference (STL/CLR)
ms.assetid: fb2bf992-d410-4b93-b087-cf2ac4b12e87
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multiset::reference (STL-CLR)
The type of a reference to an element.  
  
## Syntax  
  
```  
typedef value_type% reference;  
```  
  
## Remarks  
 The type describes a reference to an element.  
  
## Example  
  
```  
// cliext_multiset_reference.cpp   
// compile with: /clr   
#include <cliext/set>   
  
typedef cliext::multiset<wchar_t> Mymultiset;   
int main()   
    {   
    Mymultiset c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display initial contents " a b c"   
    Mymultiset::iterator it = c1.begin();   
    for (; it != c1.end(); ++it)   
        {   // get a reference to an element   
        Mymultiset::reference ref = *it;   
        System::Console::Write(" {0}", ref);   
        }   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a b c**   
## Requirements  
 **Header:** <cliext/set>  
  
 **Namespace:** cliext  
  
## See Also  
 [multiset](../Topic/multiset%20\(STL-CLR\).md)   
 [const_reference](../vs140/multiset--const_reference--STL-CLR-.md)   
 [value_type](../vs140/multiset--value_type--STL-CLR-.md)