---
title: "adjacent_find (STL-CLR)"
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
H1: adjacent_find (STL/CLR)
ms.assetid: 48bf57ea-b128-4d16-97c5-01d8a378369f
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# adjacent_find (STL-CLR)
Searches for two adjacent elements that are either equal or satisfy a specified condition.  
  
## Syntax  
  
```  
template<class _FwdIt> inline  
    _FwdIt adjacent_find(_FwdIt _First, _FwdIt _Last);  
template<class _FwdIt, class _Pr> inline  
    _FwdIt adjacent_find(_FwdIt _First, _FwdIt _Last, _Pr _Pred);  
```  
  
## Remarks  
 This function behaves the same as the STL function `adjacent_find`. For more information, see [adjacent_find](../vs140/adjacent_find.md).  
  
## Requirements  
 **Header:** <cliext/algorithm>  
  
 **Namespace:** cliext  
  
## See Also  
 [algorithm (STL/CLR)](../vs140/algorithm--STL-CLR-.md)