---
title: "operator&lt;= (pair) (STL-CLR)"
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
H1: operator&lt;= (pair) (STL/CLR)
ms.assetid: 94a4cc0a-cef4-4050-bd59-f826bd318e7b
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator&lt;= (pair) (STL-CLR)
Pair less than or equal comparison.  
  
## Syntax  
  
```  
template<typename Value1,  
    typename Value2>  
    bool operator<=(pair<Value1, Value2>% left,  
        pair<Value1, Value2>% right);  
```  
  
#### Parameters  
 left  
 Left pair to compare.  
  
 right  
 Right pair to compare.  
  
## Remarks  
 The operator function returns `!(``right` `<` `left``)`. You use it to test whether `left` is not ordered after `right` when the two pairs are compared element by element.  
  
## Example  
  
```  
// cliext_pair_operator_le.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
    cliext::pair<wchar_t, int> c2(L'x', 4);   
    System::Console::WriteLine("[{0}, {1}]", c2.first, c2.second);   
  
    System::Console::WriteLine("[x 3] <= [x 3] is {0}",   
        c1 <= c1);   
    System::Console::WriteLine("[x 4] <= [x 3] is {0}",   
        c2 <= c1);   
    return (0);   
    }  
  
```  
  
 **[x, 3]**  
**[x, 4]**  
**[x 3] <= [x 3] is True**  
**[x 4] <= [x 3] is False**   
## Requirements  
 **Header:** <cliext/utility>  
  
 **Namespace:** cliext  
  
## See Also  
 [pair](../vs140/pair--STL-CLR-.md)   
 [operator==](../vs140/operator==--pair---STL-CLR-.md)   
 [operator!=](../vs140/operator!=--pair---STL-CLR-.md)   
 [operator<](../vs140/operator---pair---STL-CLR-.md)   
 [operator>=](../vs140/operator-=--pair---STL-CLR-.md)   
 [operator>](../vs140/operator---pair---STL-CLR-.md)