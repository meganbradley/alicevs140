---
title: "list::back (STL-CLR)"
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
H1: list::back (STL/CLR)
ms.assetid: 3241e497-42ab-4108-8598-3f90eac76f07
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::back (STL-CLR)
Accesses the last element.  
  
## Syntax  
  
```  
reference back();  
```  
  
## Remarks  
 The member function returns a reference to the last element of the controlled sequence, which must be non-empty. You use it to access the last element, when you know it exists.  
  
## Example  
  
```  
// cliext_list_back.cpp   
// compile with: /clr   
#include <cliext/list>   
  
int main()   
    {   
    cliext::list<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// inspect last item   
    System::Console::WriteLine("back() = {0}", c1.back());   
  
// alter last item and reinspect   
    c1.back() = L'x';   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a b c**  
**back() = c**  
 **a b x**   
## Requirements  
 **Header:** <cliext/list>  
  
 **Namespace:** cliext  
  
## See Also  
 [list](../Topic/list%20\(STL-CLR\).md)   
 [back_item](../vs140/list--back_item--STL-CLR-.md)   
 [front](../vs140/list--front--STL-CLR-.md)   
 [front_item](../vs140/list--front_item--STL-CLR-.md)