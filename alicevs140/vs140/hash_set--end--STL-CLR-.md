---
title: "hash_set::end (STL-CLR)"
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
H1: hash_set::end (STL/CLR)
ms.assetid: 957de04e-fdc1-4295-ba25-8b0ad1ea97de
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_set::end (STL-CLR)
Designates the end of the controlled sequence.  
  
## Syntax  
  
```  
iterator end();  
```  
  
## Remarks  
 The member function returns a bidirectional iterator that points just beyond the end of the controlled sequence. You use it to obtain an iterator that designates the end of the controlled sequence; its status doesn not change if the length of the controlled sequence changes.  
  
## Example  
  
```  
// cliext_hash_set_end.cpp   
// compile with: /clr   
#include <cliext/hash_set>   
  
typedef cliext::hash_set<wchar_t> Myhash_set;   
int main()   
    {   
    Myhash_set c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// inspect last two items   
    Myhash_set::iterator it = c1.end();   
    --it;   
    System::Console::WriteLine("*-- --end() = {0}", *--it);   
    System::Console::WriteLine("*--end() = {0}", *++it);   
    return (0);   
    }  
  
```  
  
  **a b c**  
**\*-- --end() = b**  
**\*--end() = c**   
## Requirements  
 **Header:** <cliext/hash_set>  
  
 **Namespace:** cliext  
  
## See Also  
 [hash_set](../Topic/hash_set%20\(STL-CLR\).md)   
 [begin](../vs140/hash_set--begin--STL-CLR-.md)