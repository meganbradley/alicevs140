---
title: "queue::push (STL-CLR)"
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
H1: queue::push (STL/CLR)
ms.assetid: 97cf1f98-d4c4-417f-b57a-89cdd351ef65
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# queue::push (STL-CLR)
Adds a new last element.  
  
## Syntax  
  
```  
void push(value_type val);  
```  
  
## Remarks  
 The member function adds an element with value `val` at the end of the queue. You use it to append an element to the queue.  
  
## Example  
  
```  
// cliext_queue_push.cpp   
// compile with: /clr   
#include <cliext/queue>   
  
typedef cliext::queue<wchar_t> Myqueue;   
int main()   
    {   
    Myqueue c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a b c**   
## Requirements  
 **Header:** <cliext/queue>  
  
 **Namespace:** cliext  
  
## See Also  
 [queue](../Topic/queue%20\(STL-CLR\).md)   
 [pop](../vs140/queue--pop--STL-CLR-.md)