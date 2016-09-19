---
title: "hash_set::value_type (STL-CLR)"
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
H1: hash_set::value_type (STL/CLR)
ms.assetid: a83724eb-496a-43ef-b969-b441f258e3be
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_set::value_type (STL-CLR)
The type of an element.  
  
## Syntax  
  
```  
typedef generic_value value_type;  
```  
  
## Remarks  
 The type is a synonym for `generic_value`.  
  
## Example  
  
```  
// cliext_hash_set_value_type.cpp   
// compile with: /clr   
#include <cliext/hash_set>   
  
typedef cliext::hash_set<wchar_t> Myhash_set;   
int main()   
    {   
    Myhash_set c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display contents " a b c" using value_type   
    for (Myhash_set::iterator it = c1.begin(); it != c1.end(); ++it)   
        {   // store element in value_type object   
        Myhash_set::value_type val = *it;   
  
        System::Console::Write(" {0}", val);   
        }   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a b c**   
## Requirements  
 **Header:** <cliext/hash_set>  
  
 **Namespace:** cliext  
  
## See Also  
 [hash_set](../Topic/hash_set%20\(STL-CLR\).md)   
 [const_reference](../vs140/hash_set--const_reference--STL-CLR-.md)   
 [key_type](../vs140/hash_set--key_type--STL-CLR-.md)   
 [reference](../vs140/hash_set--reference--STL-CLR-.md)