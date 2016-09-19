---
title: "deque::erase (STL-CLR)"
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
H1: deque::erase (STL/CLR)
ms.assetid: 831fbc2b-604f-446b-88bc-b37531304c33
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# deque::erase (STL-CLR)
Removes elements at specified positions.  
  
## Syntax  
  
```  
iterator erase(iterator where);  
iterator erase(iterator first, iterator last);  
```  
  
#### Parameters  
 first  
 Beginning of range to erase.  
  
 last  
 End of range to erase.  
  
 where  
 Element to erase.  
  
## Remarks  
 The first member function removes the element of the controlled sequence pointed to by `where`. You use it to remove a single element.  
  
 The second member function removes the elements of the controlled sequence in the range `[``first``,` `last``)`. You use it to remove zero or more contiguous elements.  
  
 Both member functions return an iterator that designates the first element remaining beyond any elements removed, or [end](../vs140/deque--end--STL-CLR-.md)`()` if no such element exists.  
  
 When erasing elements, the number of element copies is linear in the number of elements between the end of the erasure and the nearer end of the sequence. (When erasing one or more elements at either end of the sequence, no element copies occur.)  
  
## Example  
  
```  
// cliext_deque_erase.cpp   
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
  
// erase an element and reinspect   
    System::Console::WriteLine("erase(begin()) = {0}",   
        *c1.erase(c1.begin()));   
  
// add elements and display " b c d e"   
    c1.push_back(L'd');   
    c1.push_back(L'e');   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// erase all but end   
    cliext::deque<wchar_t>::iterator it = c1.end();   
    System::Console::WriteLine("erase(begin(), end()-1) = {0}",   
        *c1.erase(c1.begin(), --it));   
    System::Console::WriteLine("size() = {0}", c1.size());   
    return (0);   
    }  
  
```  
  
  **a b c**  
**erase(begin()) = b**  
 **b c d e**  
**erase(begin(), end()-1) = e**  
**size() = 1**   
## Requirements  
 **Header:** <cliext/deque>  
  
 **Namespace:** cliext  
  
## See Also  
 [deque](../Topic/deque%20\(STL-CLR\).md)   
 [clear](../vs140/deque--clear--STL-CLR-.md)