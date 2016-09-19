---
title: "hash_multimap::value_compare (STL-CLR)"
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
H1: hash_multimap::value_compare (STL/CLR)
ms.assetid: 64daa1b6-3019-4850-9ec5-ae63c01fe819
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_multimap::value_compare (STL-CLR)
The ordering delegate for two element values.  
  
## Syntax  
  
```  
Microsoft::VisualC::StlClr::BinaryDelegate<generic_value, generic_value, bool>  
    value_compare;  
```  
  
## Remarks  
 The type is a synonym for the delegate that determines the ordering of its value arguments.  
  
## Example  
  
```  
// cliext_hash_multimap_value_compare.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_map<wchar_t, int> Myhash_multimap;   
int main()   
    {   
    Myhash_multimap c1;   
    Myhash_multimap::value_compare^ kcomp = c1.value_comp();   
  
    System::Console::WriteLine("compare([L'a', 1], [L'a', 1]) = {0}",   
        kcomp(Myhash_multimap::make_value(L'a', 1),   
            Myhash_multimap::make_value(L'a', 1)));   
    System::Console::WriteLine("compare([L'a', 1], [L'b', 2]) = {0}",   
        kcomp(Myhash_multimap::make_value(L'a', 1),   
            Myhash_multimap::make_value(L'b', 2)));   
    System::Console::WriteLine("compare([L'b', 2], [L'a', 1]) = {0}",   
        kcomp(Myhash_multimap::make_value(L'b', 2),   
            Myhash_multimap::make_value(L'a', 1)));   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
 **compare([L'a', 1], [L'a', 1]) = True**  
**compare([L'a', 1], [L'b', 2]) = True**  
**compare([L'b', 2], [L'a', 1]) = False**   
## Requirements  
 **Header:** <cliext/hash_map>  
  
 **Namespace:** cliext  
  
## See Also  
 [hash_multimap](../Topic/hash_multimap%20\(STL-CLR\).md)   
 [key_compare](../vs140/hash_multimap--key_compare--STL-CLR-.md)   
 [value_comp](../vs140/hash_multimap--value_comp--STL-CLR-.md)   
 [value_type](../vs140/hash_multimap--value_type--STL-CLR-.md)