---
title: "stack::get_container (STL-CLR)"
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
H1: stack::get_container (STL/CLR)
ms.assetid: ba6fc541-fc18-4d1c-8e3f-6baaed427cbb
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# stack::get_container (STL-CLR)
Accesses the underlying container.  
  
## Syntax  
  
```  
container_type^ get_container();  
```  
  
## Remarks  
 The member function returns a handle for underlying container. You use it to bypass the restrictions imposed by the container wrapper.  
  
## Example  
  
```  
// cliext_stack_get_container.cpp   
// compile with: /clr   
#include <cliext/stack>   
  
typedef cliext::stack<wchar_t> Mystack;   
int main()   
    {   
    Mystack c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display contents " a b c" using container_type   
    Mystack::container_type wc1 = c1.get_container();   
    for each (wchar_t elem in wc1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a b c**   
## Requirements  
 **Header:** <cliext/stack>  
  
 **Namespace:** cliext  
  
## See Also  
 [stack](../Topic/stack%20\(STL-CLR\).md)   
 [container_type](../vs140/stack--container_type--STL-CLR-.md)