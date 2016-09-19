---
title: "hash_map::find (STL-CLR)"
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
H1: hash_map::find (STL/CLR)
ms.assetid: 53ff8d57-2ea4-485e-9419-aed5e3f5affb
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_map::find (STL-CLR)
Finds an element that matches a specified key.  
  
## Syntax  
  
```  
iterator find(key_type key);  
```  
  
#### Parameters  
 key  
 Key value to search for.  
  
## Remarks  
 If at least one element in the controlled sequence has equivalent ordering with `key`, the member function returns an iterator designating one of those elements; otherwise it returns [end](../vs140/hash_map--end--STL-CLR-.md)`()`. You use it to locate an element currently in the controlled sequence that matches a specified key.  
  
## Example  
  
```  
// cliext_hash_map_find.cpp   
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
  
    System::Console::WriteLine("find {0} = {1}",   
        L'A', c1.find(L'A') != c1.end());   
  
    Myhash_map::iterator it = c1.find(L'b');   
    System::Console::WriteLine("find {0} = [{1} {2}]",   
        L'b', it->first, it->second);   
  
    System::Console::WriteLine("find {0} = {1}",   
        L'C', c1.find(L'C') != c1.end());   
    return (0);   
    }  
  
```  
  
  **[a 1] [b 2] [c 3]**  
**find A = False**  
**find b = [b 2]**  
**find C = False**   
## Description  
 Note that `find` does not guarantee which of several element it finds.  
  
## Requirements  
 **Header:** <cliext/hash_map>  
  
 **Namespace:** cliext  
  
## See Also  
 [hash_map](../Topic/hash_map%20\(STL-CLR\).md)   
 [equal_range](../vs140/hash_map--equal_range--STL-CLR-.md)   
 [lower_bound](../vs140/hash_map--lower_bound--STL-CLR-.md)   
 [upper_bound](../vs140/hash_map--upper_bound--STL-CLR-.md)