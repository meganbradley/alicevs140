---
title: "priority_queue::top_item (STL-CLR)"
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
H1: priority_queue::top_item (STL/CLR)
ms.assetid: d497403b-6b1d-4c6e-a0f4-c744cc5fad75
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# priority_queue::top_item (STL-CLR)
Accesses the highest-priority element.  
  
## Syntax  
  
```  
property value_type back_item;  
```  
  
## Remarks  
 The property accesses the top (highest-priority) element of the controlled sequence, which must be non-empty. You use it to read or write the highest-priority element, when you know it exists.  
  
## Example  
  
```  
// cliext_priority_queue_top_item.cpp   
// compile with: /clr   
#include <cliext/queue>   
  
typedef cliext::priority_queue<wchar_t> Mypriority_queue;   
int main()   
    {   
    Mypriority_queue c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// inspect last item   
    System::Console::WriteLine("top_item = {0}", c1.top_item);   
  
// alter last item and reinspect   
    c1.top_item = L'x';   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **c a b**  
**top_item = c**  
 **x a b**   
## Requirements  
 **Header:** <cliext/queue>  
  
 **Namespace:** cliext  
  
## See Also  
 [priority_queue](../Topic/priority_queue%20\(STL-CLR\).md)   
 [top](../vs140/priority_queue--top--STL-CLR-.md)