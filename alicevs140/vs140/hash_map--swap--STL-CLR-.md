---
title: "hash_map::swap (STL-CLR)"
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
H1: hash_map::swap (STL/CLR)
ms.assetid: bc1349e0-9be2-4767-a87b-4834615cb52a
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_map::swap (STL-CLR)
Swaps the contents of two containers.  
  
## Syntax  
  
```  
void swap(hash_map<Key, Mapped>% right);  
```  
  
#### Parameters  
 right  
 Container to swap contents with.  
  
## Remarks  
 The member function swaps the controlled sequences between `this` and `right`. It does so in constant time and it throws no exceptions. You use it as a quick way to exchange the contents of two containers.  
  
## Example  
  
```  
// cliext_hash_map_swap.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_map<wchar_t, int> Myhash_map;   
int main()   
    {   
    Myhash_map c1;   
    c1.insert(Myhash_map::make_value(L'a', 1));   
    c1.insert(Myhash_map::make_value(L'b', 2));   
    c1.insert(Myhash_map::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Myhash_map::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct another container with repetition of values   
    Myhash_map c2;   
    c2.insert(Myhash_map::make_value(L'd', 4));   
    c2.insert(Myhash_map::make_value(L'e', 5));   
    c2.insert(Myhash_map::make_value(L'f', 6));   
    for each (Myhash_map::value_type elem in c2)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// swap and redisplay   
    c1.swap(c2);   
    for each (Myhash_map::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
    for each (Myhash_map::value_type elem in c2)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **[a 1] [b 2] [c 3]**  
 **[d 4] [e 5] [f 6]**  
 **[d 4] [e 5] [f 6]**  
 **[a 1] [b 2] [c 3]**   
## Requirements  
 **Header:** <cliext/hash_map>  
  
 **Namespace:** cliext  
  
## See Also  
 [hash_map](../Topic/hash_map%20\(STL-CLR\).md)   
 [operator=](../vs140/hash_map--operator=--STL-CLR-.md)