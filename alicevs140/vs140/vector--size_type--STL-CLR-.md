---
title: "vector::size_type (STL-CLR)"
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
H1: vector::size_type (STL/CLR)
ms.assetid: 0789e887-e79a-42f9-a162-fc27f1341900
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vector::size_type (STL-CLR)
The type of a signed distance between two elements.  
  
## Syntax  
  
```  
typedef int size_type;  
```  
  
## Remarks  
 The type describes a non-negative element count.  
  
## Example  
  
```  
// cliext_vector_size_type.cpp   
// compile with: /clr   
#include <cliext/vector>   
  
int main()   
    {   
    cliext::vector<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// compute positive difference   
    cliext::vector<wchar_t>::size_type diff = c1.end() - c1.begin();   
    System::Console::WriteLine("end()-begin() = {0}", diff);   
    return (0);   
    }  
  
```  
  
  **a b c**  
**end()-begin() = 3**   
## Requirements  
 **Header:** <cliext/vector>  
  
 **Namespace:** cliext  
  
## See Also  
 [vector](../Topic/vector%20\(STL-CLR\).md)   
 [empty](../vs140/vector--empty--STL-CLR-.md)