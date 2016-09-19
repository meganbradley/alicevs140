---
title: "list::unique (STL-CLR)"
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
H1: list::unique (STL/CLR)
ms.assetid: c3a29e4e-0ec1-4472-b050-7a9511037132
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::unique (STL-CLR)
Removes adjacent elements that pass a specified test.  
  
## Syntax  
  
```  
void unique();  
template<typename Pred2>  
    void unique(Pred2 pred);  
```  
  
#### Parameters  
 pred  
 Comparer for element pairs.  
  
## Remarks  
 The first member function removes from the controlled sequence (erases) every element that compares equal to its preceding element -- if element `X` precedes element `Y` and `X == Y`, the member function removes `Y`. You use it to remove all but one copy of every subsequence of adjacent elements that compare equal. Note that if the controlled sequence is ordered, such as by calling [sort](../vs140/list--sort--STL-CLR-.md)`()`, the member function leaves only elements with unique values. (Hence the name).  
  
 The second member function behaves the same as the first, except that it removes each element `Y` following an element `X` for which `pred``(X, Y)`. You use it to remove all but one copy of every subsequence of adjacent elements that satisfy a predicate function or delegate that you specify. Note that if the controlled sequence is ordered, such as by calling `sort(``pred``)`, the member function leaves only elements that do not have equivalent ordering with any other elements.  
  
## Example  
  
```  
// cliext_list_unique.cpp   
// compile with: /clr   
#include <cliext/list>   
  
int main()   
    {   
    cliext::list<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display initial contents " a a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// display contents after unique   
    cliext::list<wchar_t> c2(c1);   
    c2.unique();   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// display contents after unique(not_equal_to)   
    c2 = c1;   
    c2.unique(cliext::not_equal_to<wchar_t>());   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a a b c**  
 **a b c**  
 **a a**   
## Requirements  
 **Header:** <cliext/list>  
  
 **Namespace:** cliext  
  
## See Also  
 [list](../Topic/list%20\(STL-CLR\).md)   
 [remove](../vs140/list--remove--STL-CLR-.md)   
 [remove_if](../vs140/list--remove_if--STL-CLR-.md)   
 [sort](../vs140/list--sort--STL-CLR-.md)