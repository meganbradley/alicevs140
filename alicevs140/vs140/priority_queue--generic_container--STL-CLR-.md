---
title: "priority_queue::generic_container (STL-CLR)"
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
H1: priority_queue::generic_container (STL/CLR)
ms.assetid: b938c433-7ef1-4077-93c2-2aee8ddf4d67
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# priority_queue::generic_container (STL-CLR)
The type of the generic interface for the container.  
  
## Syntax  
  
```  
typedef Microsoft::VisualC::StlClr::IPriorityQueue<Value>  
    generic_container;  
```  
  
## Remarks  
 The type describes the generic interface for this template container adapter class.  
  
## Example  
  
```  
// cliext_priority_queue_generic_container.cpp   
// compile with: /clr   
#include <cliext/queue>   
  
typedef cliext::priority_queue<wchar_t> Mypriority_queue;   
int main()   
    {   
    Mypriority_queue c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct a generic container   
    Mypriority_queue::generic_container^ gc1 = %c1;   
    for each (wchar_t elem in gc1->get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// modify generic and display original   
    gc1->push(L'd');   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// modify original and display generic   
    c1.push(L'e');   
    for each (wchar_t elem in gc1->get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **c a b**  
 **c a b**  
 **d c b a**  
 **e d b a c**   
## Requirements  
 **Header:** <cliext/queue>  
  
 **Namespace:** cliext  
  
## See Also  
 [priority_queue](../Topic/priority_queue%20\(STL-CLR\).md)