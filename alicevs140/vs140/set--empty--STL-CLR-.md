---
title: "set::empty (STL-CLR)"
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
H1: set::empty (STL/CLR)
ms.assetid: af10279f-e9e8-4599-b59b-5b8d92b619eb
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# set::empty (STL-CLR)
Tests whether no elements are present.  
  
## Syntax  
  
```  
bool empty();  
```  
  
## Remarks  
 The member function returns true for an empty controlled sequence. It is equivalent to [size](../vs140/set--size--STL-CLR-.md)`() == 0`. You use it to test whether the set is empty.  
  
## Example  
  
```  
// cliext_set_empty.cpp   
// compile with: /clr   
#include <cliext/set>   
  
typedef cliext::set<wchar_t> Myset;   
int main()   
    {   
    Myset c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    System::Console::WriteLine("size() = {0}", c1.size());   
    System::Console::WriteLine("empty() = {0}", c1.empty());   
  
// clear the container and reinspect   
    c1.clear();   
    System::Console::WriteLine("size() = {0}", c1.size());   
    System::Console::WriteLine("empty() = {0}", c1.empty());   
    return (0);   
    }  
  
```  
  
  **a b c**  
**size() = 3**  
**empty() = False**  
**size() = 0**  
**empty() = True**   
## Requirements  
 **Header:** <cliext/set>  
  
 **Namespace:** cliext  
  
## See Also  
 [set](../Topic/set%20\(STL-CLR\).md)   
 [size](../vs140/set--size--STL-CLR-.md)