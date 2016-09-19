---
title: "list::splice (STL-CLR)"
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
H1: list::splice (STL/CLR)
ms.assetid: ebc424b9-8341-4a88-b101-86d56324f5ac
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::splice (STL-CLR)
Restitch links between nodes.  
  
## Syntax  
  
```  
void splice(iterator where, list<Value>% right);  
void splice(iterator where, list<Value>% right,  
    iterator first);  
void splice(iterator where, list<Value>% right,  
    iterator first, iterator last);  
```  
  
#### Parameters  
 first  
 Beginning of range to splice.  
  
 last  
 End of range to splice.  
  
 right  
 Container to splice from.  
  
 where  
 Where in container to splice before.  
  
## Remarks  
 The first member function inserts the sequence controlled by `right` before the element in the controlled sequence pointed to by `where`. It also removes all elements from `right`. (`%``right` must not equal `this`.) You use it to splice all of one list into another.  
  
 The second member function removes the element pointed to by `first` in the sequence controlled by `right` and inserts it before the element in the controlled sequence pointed to by `where`. (If `where` `==` `first` `||` `where` `== ++``first`, no change occurs.) You use it to splice a single element of one list into another.  
  
 The third member function inserts the subrange designated by `[``first``,` `last``)` from the sequence controlled by `right` before the element in the controlled sequence pointed to by `where`. It also removes the original subrange from the sequence controlled by `right`. (If `right` `==` `this`, the range `[``first``,` `last``)` must not include the element pointed to by `where`.) You use it to splice a subsequence of zero or more elements from one list into another.  
  
## Example  
  
```  
// cliext_list_splice.cpp   
// compile with: /clr   
#include <cliext/list>   
  
int main()   
    {   
    cliext::list<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// splice to a new list   
    cliext::list<wchar_t> c2;   
    c2.splice(c2.begin(), c1);   
    System::Console::WriteLine("c1.size() = {0}", c1.size());   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// return one element   
    c1.splice(c1.end(), c2, c2.begin());   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// return remaining elements   
    c1.splice(c1.begin(), c2, c2.begin(), c2.end());   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    System::Console::WriteLine("c2.size() = {0}", c2.size());   
    return (0);   
    }  
  
```  
  
  **a b c**  
**c1.size() = 0**  
 **a b c**  
 **a**  
 **b c**  
 **b c a**  
**c2.size() = 0**   
## Requirements  
 **Header:** <cliext/list>  
  
 **Namespace:** cliext  
  
## See Also  
 [list](../Topic/list%20\(STL-CLR\).md)   
 [assign](../vs140/list--assign--STL-CLR-.md)   
 [insert](../vs140/list--insert--STL-CLR-.md)   
 [merge](../vs140/list--merge--STL-CLR-.md)