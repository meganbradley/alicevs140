---
title: "list::remove_if (STL-CLR)"
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
H1: list::remove_if (STL/CLR)
ms.assetid: cbc66192-751b-41c5-b557-d5d7bbc2a840
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::remove_if (STL-CLR)
Removes elements that pass a specified test.  
  
## Syntax  
  
```  
template<typename Pred1>  
    void remove_if(Pred1 pred);  
```  
  
#### Parameters  
 pred  
 Test for elements to remove.  
  
## Remarks  
 The member function removes from the controlled sequence (erases) every element `X` for which `pred``(X)` is true. You use it to remove all elements that satisfy a condition you specify as a function or delegate.  
  
## Example  
  
```  
// cliext_list_remove_if.cpp   
// compile with: /clr   
#include <cliext/list>   
  
int main()   
    {   
    cliext::list<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'b');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display initial contents " a b b b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// fail to remove and redisplay   
    c1.remove_if(cliext::binder2nd<cliext::equal_to<wchar_t> >(   
        cliext::equal_to<wchar_t>(), L'd'));   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// remove and redisplay   
    c1.remove_if(cliext::binder2nd<cliext::not_equal_to<wchar_t> >(   
        cliext::not_equal_to<wchar_t>(), L'b'));   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a b b b c**  
 **a b b b c**  
 **b b b**   
## Requirements  
 **Header:** <cliext/list>  
  
 **Namespace:** cliext  
  
## See Also  
 [list](../Topic/list%20\(STL-CLR\).md)   
 [clear](../vs140/list--clear--STL-CLR-.md)   
 [erase](../vs140/list--erase--STL-CLR-.md)   
 [remove](../vs140/list--remove--STL-CLR-.md)   
 [unique](../vs140/list--unique--STL-CLR-.md)