---
title: "operator&gt;= (vector) (STL-CLR)"
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
H1: operator&gt;= (vector) (STL/CLR)
ms.assetid: c06f4489-f65a-4bd6-944f-9b23a2bb4e35
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator&gt;= (vector) (STL-CLR)
Vector greater than or equal comparison.  
  
## Syntax  
  
```  
template<typename Value>  
    bool operator>=(vector<Value>% left,  
        vector<Value>% right);  
```  
  
#### Parameters  
 left  
 Left container to compare.  
  
 right  
 Right container to compare.  
  
## Remarks  
 The operator function returns `!(``left` `<` `right``)`. You use it to test whether `left` is not ordered before `right` when the two vectors are compared element by element.  
  
## Example  
  
```  
// cliext_vector_operator_ge.cpp   
// compile with: /clr   
#include <cliext/vector>   
  
int main()   
    {   
    cliext::vector<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign to a new container   
    cliext::vector<wchar_t> c2;   
    c2.push_back(L'a');   
    c2.push_back(L'b');   
    c2.push_back(L'd');   
  
// display contents " a b d"   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    System::Console::WriteLine("[a b c] >= [a b c] is {0}",   
        c1 >= c1);   
    System::Console::WriteLine("[a b c] >= [a b d] is {0}",   
        c1 >= c2);   
    return (0);   
    }  
  
```  
  
  **a b c**  
 **a b d**  
**[a b c] >= [a b c] is True**  
**[a b c] >= [a b d] is False**   
## Requirements  
 **Header:** <cliext/vector>  
  
 **Namespace:** cliext  
  
## See Also  
 [vector](../Topic/vector%20\(STL-CLR\).md)   
 [operator==](../vs140/operator==--vector---STL-CLR-.md)   
 [operator!=](../vs140/operator!=--vector---STL-CLR-.md)   
 [operator<](../vs140/operator---vector---STL-CLR-.md)   
 [operator>](../vs140/operator---vector---STL-CLR-.md)   
 [operator<=](../vs140/operator-=--vector---STL-CLR-.md)