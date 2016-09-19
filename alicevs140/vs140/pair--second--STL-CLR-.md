---
title: "pair::second (STL-CLR)"
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
H1: pair::second (STL/CLR)
ms.assetid: f30d3d1f-c7be-45d2-92ff-6861b96a92ff
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# pair::second (STL-CLR)
The second wrapped value.  
  
## Syntax  
  
```  
Value2 second;  
```  
  
## Remarks  
 The object stores the second wrapped value.  
  
## Example  
  
```  
// cliext_pair_second.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
  
    cliext::pair<wchar_t, int>::first_type first_val = c1.first;   
    cliext::pair<wchar_t, int>::second_type second_val = c1.second;   
    System::Console::WriteLine("[{0}, {1}]", first_val, second_val);   
    return (0);   
    }  
  
```  
  
 **[x, 3]**   
## Requirements  
 **Header:** <cliext/utility>  
  
 **Namespace:** cliext  
  
## See Also  
 [pair](../vs140/pair--STL-CLR-.md)   
 [first](../vs140/pair--first--STL-CLR-.md)   
 [first_type](../vs140/pair--first_type--STL-CLR-.md)   
 [second_type](../vs140/pair--second_type--STL-CLR-.md)