---
title: "collection_adapter::base (STL-CLR)"
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
H1: collection_adapter::base (STL/CLR)
ms.assetid: 44928046-3fda-4974-817f-bc61a6f11b9f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# collection_adapter::base (STL-CLR)
Designates the wrapped BCL interface.  
  
## Syntax  
  
```  
Coll^ base();  
```  
  
## Remarks  
 The member function returns the stored BCL interface handle.  
  
## Example  
  
```  
// cliext_collection_adapter_base.cpp   
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
  
    System::Console::WriteLine("base() same = {0}", c1.base() == %c1);   
    return (0);   
    }  
  
```  
  
  **x x x x x x**  
**base() same = True**   
## Requirements  
 **Header:** <cliext/adapter>  
  
 **Namespace:** cliext  
  
## See Also  
 [collection_adapter](../vs140/collection_adapter--STL-CLR-.md)