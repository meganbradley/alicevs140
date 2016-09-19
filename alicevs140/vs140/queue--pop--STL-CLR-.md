---
title: "queue::pop (STL-CLR)"
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
H1: queue::pop (STL/CLR)
ms.assetid: 38f6c03b-e8f8-4663-b3d6-18314cdc8e7d
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# queue::pop (STL-CLR)
Removes the last element.  
  
## Syntax  
  
```  
void pop();  
```  
  
## Remarks  
 The member function removes the last element of the controlled sequence, which must be non-empty. You use it to shorten the queue by one element at the back.  
  
## Example  
  
```  
// cliext_queue_pop.cpp   
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
  
// pop an element and redisplay   
    c1.pop();   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a b c**  
 **b c**   
## Requirements  
 **Header:** <cliext/queue>  
  
 **Namespace:** cliext  
  
## See Also  
 [queue](../Topic/queue%20\(STL-CLR\).md)   
 [push](../vs140/queue--push--STL-CLR-.md)