---
title: "operator!= (stack) (STL-CLR)"
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
H1: operator!= (stack) (STL/CLR)
ms.assetid: d28aca6a-685c-4d3d-bc97-de80d75ccd60
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator!= (stack) (STL-CLR)
Stack not equal comparison.  
  
## Syntax  
  
```  
template<typename Value,  
    typename Container>  
    bool operator!=(stack<Value, Container>% left,  
        stack<Value, Container>% right);  
```  
  
#### Parameters  
 left  
 Left container to compare.  
  
 right  
 Right container to compare.  
  
## Remarks  
 The operator function returns `!(``left` `==` `right``)`. You use it to test whether `left` is not ordered the same as `right` when the two stacks are compared element by element.  
  
## Example  
  
```  
// cliext_stack_operator_ne.cpp   
// compile with: /clr   
#include <cliext/stack>   
  
typedef cliext::stack<wchar_t> Mystack;   
int main()   
    {   
    Mystack c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign to a new container   
    Mystack c2;   
    c2.push(L'a');   
    c2.push(L'b');   
    c2.push(L'd');   
  
// display contents " a b d"   
    for each (wchar_t elem in c2.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    System::Console::WriteLine("[a b c] != [a b c] is {0}",   
        c1 != c1);   
    System::Console::WriteLine("[a b c] != [a b d] is {0}",   
        c1 != c2);   
    return (0);   
    }  
  
```  
  
  **a b c**  
 **a b d**  
**[a b c] != [a b c] is False**  
**[a b c] != [a b d] is True**   
## Requirements  
 **Header:** <cliext/stack>  
  
 **Namespace:** cliext  
  
## See Also  
 [stack](../Topic/stack%20\(STL-CLR\).md)   
 [operator==](../vs140/operator==--stack---STL-CLR-.md)   
 [operator<](../vs140/operator---stack---STL-CLR-.md)   
 [operator>=](../vs140/operator-=--stack---STL-CLR-.md)   
 [operator>](../vs140/operator---stack---STL-CLR-.md)   
 [operator<=](../vs140/operator-=--stack---STL-CLR-.md)