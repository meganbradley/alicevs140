---
title: "deque::pop_front (STL-CLR)"
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
H1: deque::pop_front (STL/CLR)
ms.assetid: 5042df47-b226-4b16-982e-6a4543b8e00b
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# deque::pop_front (STL-CLR)
Removes the first element.  
  
## Syntax  
  
```  
void pop_front();  
```  
  
## Remarks  
 The member function removes the first element of the controlled sequence, which must be non-empty. You use it to shorten the deque by one element at the front.  
  
## Example  
  
```  
// cliext_deque_pop_front.cpp   
// compile with: /clr   
#include <cliext/deque>   
  
int main()   
    {   
    cliext::deque<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// pop an element and redisplay   
    c1.pop_front();   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a b c**  
 **b c**   
## Requirements  
 **Header:** <cliext/deque>  
  
 **Namespace:** cliext  
  
## See Also  
 [deque](../Topic/deque%20\(STL-CLR\).md)   
 [pop_back](../vs140/deque--pop_back--STL-CLR-.md)   
 [push_back](../vs140/deque--push_back--STL-CLR-.md)   
 [push_front](../vs140/deque--push_front--STL-CLR-.md)