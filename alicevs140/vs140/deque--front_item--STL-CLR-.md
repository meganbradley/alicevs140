---
title: "deque::front_item (STL-CLR)"
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
H1: deque::front_item (STL/CLR)
ms.assetid: 6243e52d-47fb-45d8-ade8-70debd97887d
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# deque::front_item (STL-CLR)
Accesses the first element.  
  
## Syntax  
  
```  
property value_type front_item;  
```  
  
## Remarks  
 The property accesses the first element of the controlled sequence, which must be non-empty. You use it to read or write the first element, when you know it exists.  
  
## Example  
  
```  
// cliext_deque_front_item.cpp   
// compile with: /clr   
#include <cliext/deque>   
  
int main()   
    {   
    cliext::deque<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// inspect first item   
    System::Console::WriteLine("front_item = {0}", c1.front_item);   
  
// alter first item and reinspect   
    c1.front_item = L'x';   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a b c**  
**front_item = a**  
 **x b c**   
## Requirements  
 **Header:** <cliext/deque>  
  
 **Namespace:** cliext  
  
## See Also  
 [deque](../Topic/deque%20\(STL-CLR\).md)   
 [back](../vs140/deque--back--STL-CLR-.md)   
 [back_item](../vs140/deque--back_item--STL-CLR-.md)   
 [front](../vs140/deque--front--STL-CLR-.md)