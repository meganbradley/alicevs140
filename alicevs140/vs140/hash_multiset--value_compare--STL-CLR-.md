---
title: "hash_multiset::value_compare (STL-CLR)"
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
H1: hash_multiset::value_compare (STL/CLR)
ms.assetid: 87f7df53-832b-4932-987b-1300943ad299
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_multiset::value_compare (STL-CLR)
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
// cliext_hash_multiset_value_compare.cpp   
// compile with: /clr   
#include <cliext/hash_set>   
  
typedef cliext::hash_multiset<wchar_t> Myhash_multiset;   
int main()   
    {   
    Myhash_multiset c1;   
    Myhash_multiset::value_compare^ kcomp = c1.value_comp();   
  
    System::Console::WriteLine("compare(L'a', L'a') = {0}",   
        kcomp(L'a', L'a'));   
    System::Console::WriteLine("compare(L'a', L'b') = {0}",   
        kcomp(L'a', L'b'));   
    System::Console::WriteLine("compare(L'b', L'a') = {0}",   
        kcomp(L'b', L'a'));   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
 **compare(L'a', L'a') = True**  
**compare(L'a', L'b') = True**  
**compare(L'b', L'a') = False**   
## Requirements  
 **Header:** <cliext/hash_set>  
  
 **Namespace:** cliext  
  
## See Also  
 [hash_multiset](../Topic/hash_multiset%20\(STL-CLR\).md)   
 [key_compare](../vs140/hash_multiset--key_compare--STL-CLR-.md)   
 [value_comp](../vs140/hash_multiset--value_comp--STL-CLR-.md)   
 [value_type](../vs140/hash_multiset--value_type--STL-CLR-.md)