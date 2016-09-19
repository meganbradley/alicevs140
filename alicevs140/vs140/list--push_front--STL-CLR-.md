---
title: "list::push_front (STL-CLR)"
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
H1: list::push_front (STL/CLR)
ms.assetid: 47525641-1139-44fc-ac62-bdc04876d9e0
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::push_front (STL-CLR)
Adds a new first element.  
  
## Syntax  
  
```  
void push_front(value_type val);  
```  
  
## Remarks  
 The member function inserts an element with value `val` at the beginning of the controlled sequence. You use it to prepend another element to the list.  
  
## Example  
  
```  
// cliext_list_push_front.cpp   
// compile with: /clr   
#include <cliext/list>   
  
int main()   
    {   
    cliext::list<wchar_t> c1;   
    c1.push_front(L'a');   
    c1.push_front(L'b');   
    c1.push_front(L'c');   
  
// display contents " c b a"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **c b a**   
## Requirements  
 **Header:** <cliext/list>  
  
 **Namespace:** cliext  
  
## See Also  
 [list](../Topic/list%20\(STL-CLR\).md)   
 [pop_back](../vs140/list--pop_back--STL-CLR-.md)   
 [pop_front](../vs140/list--pop_front--STL-CLR-.md)   
 [push_back](../vs140/list--push_back--STL-CLR-.md)