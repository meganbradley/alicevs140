---
title: "unique (STL-CLR)"
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
H1: unique (STL/CLR)
ms.assetid: 833cc314-b452-4659-bbb4-575c2bb63855
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unique (STL-CLR)
Removes duplicate elements that are adjacent to each other in a specified range.  
  
## Syntax  
  
```  
template<class _FwdIt> inline  
    _FwdIt unique(_FwdIt _First, _FwdIt _Last);  
template<class _FwdIt, class _Pr> inline  
    _FwdIt unique(_FwdIt _First, _FwdIt _Last, _Pr _Pred);  
```  
  
## Remarks  
 This function behaves the same as the STL function `unique`. For more information, see [unique (<algorithm\>)](../vs140/unique---algorithm--.md).  
  
## Requirements  
 **Header:** <cliext/algorithm>  
  
 **Namespace:** cliext  
  
## See Also  
 [algorithm (STL/CLR)](../vs140/algorithm--STL-CLR-.md)