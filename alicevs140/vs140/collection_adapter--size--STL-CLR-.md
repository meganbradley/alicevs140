---
title: "collection_adapter::size (STL-CLR)"
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
H1: collection_adapter::size (STL/CLR)
ms.assetid: 71866719-9e29-4572-bfb9-60321f2937c5
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# collection_adapter::size (STL-CLR)
Counts the number of elements.  
  
## Syntax  
  
```  
size_type size();  
```  
  
## Remarks  
 The member function returns the length of the controlled sequence. It is not defined in a specialization for `IEnumerable` or `IEnumerable<Value>`.  
  
## Example  
  
```  
// cliext_collection_adapter_size.cpp   
// compile with: /clr   
#include <cliext/adapter>   
#include <cliext/deque>   
  
typedef cliext::collection_adapter<   
    System::Collections::ICollection> Mycoll;   
int main()   
    {   
    cliext::deque<wchar_t> d6x(6, L'x');   
    Mycoll c1(%d6x);   
  
// display initial contents " x x x x x x"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    System::Console::WriteLine("size() = {0}", c1.size());   
    return (0);   
    }  
  
```  
  
  **x x x x x x**  
**size() = 6**   
## Requirements  
 **Header:** <cliext/adapter>  
  
 **Namespace:** cliext  
  
## See Also  
 [collection_adapter](../vs140/collection_adapter--STL-CLR-.md)