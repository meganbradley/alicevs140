---
title: "hash_multimap::load_factor (STL-CLR)"
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
H1: hash_multimap::load_factor (STL/CLR)
ms.assetid: c4b34387-fe76-405d-bead-a092b4571631
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_multimap::load_factor (STL-CLR)
Counts the average elements per bucket.  
  
## Syntax  
  
```  
float load_factor();  
```  
  
## Remarks  
 The member function returns `(float)`[size](../vs140/hash_multimap--size--STL-CLR-.md)`() /` [bucket_count](../vs140/hash_multimap--bucket_count--STL-CLR-.md)`()`. You use it to determine the average bucket size.  
  
## Example  
  
```  
// cliext_hash_multimap_load_factor.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_multimap<wchar_t, int> Myhash_multimap;   
int main()   
    {   
    Myhash_multimap c1 = gcnew Myhash_multimap;   
    c1.insert(Myhash_multimap::make_value(L'a', 1));   
    c1.insert(Myhash_multimap::make_value(L'b', 2));   
    c1.insert(Myhash_multimap::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Myhash_multimap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// inspect current parameters   
    System::Console::WriteLine("bucket_count() = {0}", c1.bucket_count());   
    System::Console::WriteLine("load_factor() = {0}", c1.load_factor());   
    System::Console::WriteLine("max_load_factor() = {0}",   
        c1.max_load_factor());   
    System::Console::WriteLine();   
  
// change max_load_factor and redisplay   
    c1.max_load_factor(0.25f);   
    System::Console::WriteLine("bucket_count() = {0}", c1.bucket_count());   
    System::Console::WriteLine("load_factor() = {0}", c1.load_factor());   
    System::Console::WriteLine("max_load_factor() = {0}",   
        c1.max_load_factor());   
    System::Console::WriteLine();   
  
// rehash and redisplay   
    c1.rehash(100);   
    System::Console::WriteLine("bucket_count() = {0}", c1.bucket_count());   
    System::Console::WriteLine("load_factor() = {0}", c1.load_factor());   
    System::Console::WriteLine("max_load_factor() = {0}",   
        c1.max_load_factor());   
    return (0);   
    }  
  
```  
  
  **[a 1] [b 2] [c 3]**  
**bucket_count() = 16**  
**load_factor() = 0.1875**  
**max_load_factor() = 4**  
**bucket_count() = 16**  
**load_factor() = 0.1875**  
**max_load_factor() = 0.25**  
**bucket_count() = 128**  
**load_factor() = 0.0234375**  
**max_load_factor() = 0.25**   
## Requirements  
 **Header:** <cliext/hash_map>  
  
 **Namespace:** cliext  
  
## See Also  
 [hash_multimap](../Topic/hash_multimap%20\(STL-CLR\).md)   
 [bucket_count](../vs140/hash_multimap--bucket_count--STL-CLR-.md)   
 [max_load_factor](../vs140/hash_multimap--max_load_factor--STL-CLR-.md)