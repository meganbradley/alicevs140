---
title: "hash_map::operator(STL-CLR)"
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
H1: hash_map::operator(STL/CLR)
ms.assetid: b0b8c1bd-4250-447d-9c69-3f8c34e9b6af
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_map::operator(STL-CLR)
Maps a key to its associated mapped value.  
  
## Syntax  
  
```  
mapped_type operator[](key_type key);  
```  
  
#### Parameters  
 key  
 Key value to search for.  
  
## Remarks  
 The member functions endeavors to find an element with equivalent ordering to `key`. If it finds one, it returns the associated mapped value; otherwise, it inserts `value_type(``key``, mapped_type())` and returns the associated (default) mapped value. You use it to look up a mapped value given its associated key, or to ensure that an entry exists for the key if none is found.  
  
## Example  
  
```  
// cliext_hash_map_operator_sub.cpp   
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
  
    System::Console::WriteLine("c1[{0}] = {1}",   
        L'A', c1[L'A']);   
    System::Console::WriteLine("c1[{0}] = {1}",   
        L'b', c1[L'b']);   
  
// redisplay altered contents   
    for each (Myhash_map::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// alter mapped values and redisplay   
    c1[L'A'] = 10;   
    c1[L'c'] = 13;   
    for each (Myhash_map::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **[a 1] [b 2] [c 3]**  
**c1[A] = 0**  
**c1[b] = 2**  
 **[a 1] [A 0] [b 2] [c 3]**  
 **[a 1] [A 10] [b 2] [c 13]**   
## Requirements  
 **Header:** <cliext/hash_map>  
  
 **Namespace:** cliext  
  
## See Also  
 [hash_map](../Topic/hash_map%20\(STL-CLR\).md)   
 [find](../vs140/hash_map--find--STL-CLR-.md)   
 [insert](../vs140/hash_map--insert--STL-CLR-.md)