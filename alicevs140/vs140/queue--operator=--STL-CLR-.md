---
title: "queue::operator= (STL-CLR)"
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
H1: queue::operator= (STL/CLR)
ms.assetid: 826c335a-5680-498c-b57d-e7bc93a914be
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# queue::operator= (STL-CLR)
Replaces the controlled sequence.  
  
## Syntax  
  
```  
queue <Value, Container>% operator=(queue <Value, Container>% right);  
```  
  
#### Parameters  
 right  
 Container adapter to copy.  
  
## Remarks  
 The member operator copies `right` to the object, then returns `*this`. You use it to replace the controlled sequence with a copy of the controlled sequence in `right`.  
  
## Example  
  
```  
// cliext_queue_operator_as.cpp   
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
  
// assign to a new container   
    Myqueue c2;   
    c2 = c1;   
    for each (wchar_t elem in c2.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a b c**  
 **a b c**   
## Requirements  
 **Header:** <cliext/queue>  
  
 **Namespace:** cliext  
  
## See Also  
 [queue](../Topic/queue%20\(STL-CLR\).md)   
 [assign](../vs140/queue--assign--STL-CLR-.md)