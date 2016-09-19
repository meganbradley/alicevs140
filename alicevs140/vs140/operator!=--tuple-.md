---
title: "operator!= &lt;tuple&gt;"
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
ms.topic: article
ms.assetid: eed1865b-bdc8-43cf-bcff-19ba73e2a322
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator!= &lt;tuple&gt;
Compare `tuple` objects for inequality.  
  
## Syntax  
  
```  
template<class T1, class T2, ..., class TN,  
    class U1, class U2, ..., class UN>  
    bool operator!=(const tuple<T1, T2, ..., TN>& tpl1,  
    const tuple<U1, U2, ..., UN>& tpl2);  
```  
  
#### Parameters  
 `TN`  
 The type of the Nth tuple element.  
  
## Remarks  
 The function returns false when `N` is 0, otherwise `get<0>(tpl1) != get<0>(tpl2) || get<1>(tpl1) != get<1>(tpl2) || ... || get<N - 1>(tpl1) == get<N - 1>(tpl2)`.  
  
## Example  
  
```  
// std_tr1__tuple__operator_ne.cpp   
// compile with: /EHsc   
#include <tuple>   
#include <iostream>   
  
typedef std::tuple<int, double, int, double> Mytuple;   
int main()   
    {   
    Mytuple c0(0, 1, 2, 3);   
  
// display contents " 0 1 2 3"   
    std::cout << " " << std::get<0>(c0);   
    std::cout << " " << std::get<1>(c0);   
    std::cout << " " << std::get<2>(c0);   
    std::cout << " " << std::get<3>(c0);   
    std::cout << std::endl;   
  
    Mytuple c1 = std::make_tuple(4, 5, 6, 7);   
  
// display contents " 4 5 6 7"   
    std::cout << " " << std::get<0>(c0);   
    std::cout << " " << std::get<1>(c0);   
    std::cout << " " << std::get<2>(c0);   
    std::cout << " " << std::get<3>(c0);   
    std::cout << std::endl;   
  
// display results of comparisons   
    std::cout << std::boolalpha << " " << (c0 != c0);   
    std::cout << std::endl;   
    std::cout << std::boolalpha << " " << (c0 != c1);   
    std::cout << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **0 1 2 3**  
 **0 1 2 3**  
 **false**  
 **true**   
## Requirements  
 **Header:** <tuple\>  
  
 **Namespace:** std  
  
## See Also  
 [<tuple\>](../vs140/-tuple-.md)   
 [operator==](../vs140/operator==--tuple-.md)   
 [operator<](../vs140/operator---tuple-.md)   
 [operator<=](../vs140/operator-=--tuple-.md)   
 [operator>](../vs140/operator---tuple-.md)   
 [operator>=](../vs140/operator-=--tuple-.md)