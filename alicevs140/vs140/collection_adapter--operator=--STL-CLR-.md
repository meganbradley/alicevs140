---
title: "collection_adapter::operator= (STL-CLR)"
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
H1: collection_adapter::operator= (STL/CLR)
ms.assetid: 45365a33-3b56-4cb7-962f-81c20d8901d3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# collection_adapter::operator= (STL-CLR)
Replaces the stored BCL handle.  
  
## Syntax  
  
```  
collection_adapter<Coll>% operator=(collection_adapter<Coll>% right);  
```  
  
#### Parameters  
 right  
 Adapter to copy.  
  
## Remarks  
 The member operator copies `right` to the object, then returns `*this`. You use it to replace the stored BCL handle with a copy of the stored BCL handle in `right`.  
  
## Example  
  
```  
// cliext_collection_adapter_operator_as.cpp   
// compile with: /clr   
#include <cliext/adapter>   
#include <cliext/deque>   
  
typedef cliext::collection_adapter<   
    System::Collections::ICollection> Mycoll;   
int main()   
    {   
    cliext::deque<wchar_t> d1;   
    d1.push_back(L'a');   
    d1.push_back(L'b');   
    d1.push_back(L'c');   
    Mycoll c1(%d1);   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign to a new container   
    Mycoll c2;   
    c2 = c1;   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a b c**  
 **a b c**   
## Requirements  
 **Header:** <cliext/adapter>  
  
 **Namespace:** cliext  
  
## See Also  
 [collection_adapter](../vs140/collection_adapter--STL-CLR-.md)