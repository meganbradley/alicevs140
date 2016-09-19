---
title: "partial_sort_copy (STL-CLR)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
H1: partial_sort_copy (STL/CLR)
ms.assetid: ed4af83e-7554-4f6d-bf54-c56fa6210fe8
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# partial_sort_copy (STL-CLR)
Copies elements from a source range into a destination range where the source elements are ordered by either less than or another specified binary predicate.  
  
## Syntax  
  
```  
template<class _InIt, class _RanIt> inline  
    _RanIt partial_sort_copy(_InIt _First1, _InIt _Last1,  
        _RanIt _First2, _RanIt _Last2);  
template<class _InIt, class _RanIt, class _Pr> inline  
    _RanIt partial_sort_copy(_InIt _First1, _InIt _Last1,  
        _RanIt _First2, _RanIt _Last2, _Pr _Pred);  
```  
  
## Remarks  
 This function behaves the same as the STL function `partial_sort_copy`. For more information, see [partial_sort_copy](../vs140/partial_sort_copy.md).  
  
## Requirements  
 **Header:** <cliext/algorithm>  
  
 **Namespace:** cliext  
  
## See Also  
 [algorithm (STL/CLR)](../vs140/algorithm--STL-CLR-.md)