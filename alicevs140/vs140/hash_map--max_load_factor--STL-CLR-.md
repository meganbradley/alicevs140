---
title: "hash_map::max_load_factor (STL-CLR)"
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
H1: hash_map::max_load_factor (STL/CLR)
ms.assetid: 7c0773c9-a918-4e61-ae95-e45148f1ff24
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_map::max_load_factor (STL-CLR)
Gets or sets the maximum elements per bucket.  
  
## Syntax  
  
```  
float max_load_factor();  
void max_load_factor(float new_factor);  
```  
  
#### Parameters  
 new_factor  
 New maximum load factor to store.  
  
## Remarks  
 The first member function returns the current stored maximum load factor. You use it to determine the maximum average bucket size.  
  
 The second member function replaces the store maximum load factor with `new_factor`. No automatic rehashing occurs until a subsequent insert.  
  
## Example  
  
```  
// cliext_hash_map_max_load_factor.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_map<wchar_t, int> Myhash_map;   
int main()   
    {   
    Myhash_map c1 = gcnew Myhash_map;   
    c1.insert(Myhash_map::make_value(L'a', 1));   
    c1.insert(Myhash_map::make_value(L'b', 2));   
    c1.insert(Myhash_map::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Myhash_map::value_type elem in c1)   
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
 [hash_map](../Topic/hash_map%20\(STL-CLR\).md)   
 [bucket_count](../vs140/hash_map--bucket_count--STL-CLR-.md)   
 [load_factor](../vs140/hash_map--load_factor--STL-CLR-.md)   
 [rehash](../vs140/hash_map--rehash--STL-CLR-.md)