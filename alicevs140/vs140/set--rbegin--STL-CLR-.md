---
title: "set::rbegin (STL-CLR)"
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
H1: set::rbegin (STL/CLR)
ms.assetid: b9da72dc-0b75-489e-b179-74c27a4bcfb7
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# set::rbegin (STL-CLR)
Designates the beginning of the reversed controlled sequence.  
  
## Syntax  
  
```  
reverse_iterator rbegin();  
```  
  
## Remarks  
 The member function returns a reverse iterator that designates the last element of the controlled sequence, or just beyond the beginning of an empty sequence. Hence, it designates the `beginning` of the reverse sequence. You use it to obtain an iterator that designates the `current` beginning of the controlled sequence seen in reverse order, but its status can change if the length of the controlled sequence changes.  
  
## Example  
  
```  
// cliext_set_rbegin.cpp   
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
  
// inspect first two items in reversed sequence   
    Myset::reverse_iterator rit = c1.rbegin();   
    System::Console::WriteLine("*rbegin() = {0}", *rit);   
    System::Console::WriteLine("*++rbegin() = {0}", *++rit);   
    return (0);   
    }  
  
```  
  
  **a b c**  
**\*rbegin() = c**  
**\*++rbegin() = b**   
## Requirements  
 **Header:** <cliext/set>  
  
 **Namespace:** cliext  
  
## See Also  
 [set](../Topic/set%20\(STL-CLR\).md)   
 [begin](../vs140/set--begin--STL-CLR-.md)   
 [end](../vs140/set--end--STL-CLR-.md)   
 [rend](../vs140/set--rend--STL-CLR-.md)