---
title: "hash_map::upper_bound (STL-CLR)"
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
H1: hash_map::upper_bound (STL/CLR)
ms.assetid: f83e88b4-e15e-49d5-90e4-cf7360c27c30
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_map::upper_bound (STL-CLR)
Finds end of range that matches a specified key.  
  
## Syntax  
  
```  
iterator upper_bound(key_type key);  
```  
  
#### Parameters  
 key  
 Key value to search for.  
  
## Remarks  
 The member function determines the last element `X` in the controlled sequence that hashes to the same bucket as `key` and has equivalent ordering to `key`. If no such element exists, or if `X` is the last element in the controlled sequence, it returns [end](../vs140/hash_map--end--STL-CLR-.md)`()`; otherwise it returns an iterator that designates the first element beyond `X`. You use it to locate the end of a sequence of elements currently in the controlled sequence that match a specified key.  
  
## Example  
  
```  
// cliext_hash_map_upper_bound.cpp   
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
  
    System::Console::WriteLine("upper_bound(L'x')==end() = {0}",   
        c1.upper_bound(L'x') == c1.end());   
  
    Myhash_map::iterator it = c1.upper_bound(L'a');   
    System::Console::WriteLine("*upper_bound(L'a') = [{0} {1}]",   
        it->first, it->second);   
    it = c1.upper_bound(L'b');   
    System::Console::WriteLine("*upper_bound(L'b') = [{0} {1}]",   
        it->first, it->second);   
    return (0);   
    }  
  
```  
  
  **[a 1] [b 2] [c 3]**  
**upper_bound(L'x')==end() = True**  
**\*upper_bound(L'a') = [b 2]**  
**\*upper_bound(L'b') = [c 3]**   
## Requirements  
 **Header:** <cliext/hash_map>  
  
 **Namespace:** cliext  
  
## See Also  
 [hash_map](../Topic/hash_map%20\(STL-CLR\).md)   
 [count](../vs140/hash_map--count--STL-CLR-.md)   
 [equal_range](../vs140/hash_map--equal_range--STL-CLR-.md)   
 [find](../vs140/hash_map--find--STL-CLR-.md)   
 [lower_bound](../vs140/hash_map--lower_bound--STL-CLR-.md)