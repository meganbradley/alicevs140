---
title: "list::size_type (STL-CLR)"
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
H1: list::size_type (STL/CLR)
ms.assetid: bfdf869f-fd7e-47b4-9ce9-68f7146dc3ed
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::size_type (STL-CLR)
The type of a signed distance between two element.  
  
## Syntax  
  
```  
typedef int size_type;  
```  
  
## Remarks  
 The type describes a non-negative element count.  
  
## Example  
  
```  
// cliext_list_size_type.cpp   
// compile with: /clr   
#include <cliext/list>   
  
int main()   
    {   
    cliext::list<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// compute positive difference   
    cliext::list<wchar_t>::size_type diff = 0;   
    for (cliext::list<wchar_t>::iterator it = c1.begin();   
        it != c1.end(); ++it)   
        ++diff;   
    System::Console::WriteLine("end()-begin() = {0}", diff);   
    return (0);   
    }  
  
```  
  
  **a b c**  
**end()-begin() = 3**   
## Requirements  
 **Header:** <cliext/list>  
  
 **Namespace:** cliext  
  
## See Also  
 [list](../Topic/list%20\(STL-CLR\).md)   
 [empty](../vs140/list--empty--STL-CLR-.md)