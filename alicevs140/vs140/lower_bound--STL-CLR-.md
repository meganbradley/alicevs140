---
title: "lower_bound (STL-CLR)"
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
H1: lower_bound (STL/CLR)
ms.assetid: 841b70b5-1f54-4ecf-8faa-7dda32a24c54
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# lower_bound (STL-CLR)
Finds the position of the first element in an ordered range that has a value less than or equivalent to a specified value, where the ordering criterion may be specified by a binary predicate.  
  
## Syntax  
  
```  
template<class _FwdIt, class _Ty> inline  
    _FwdIt lower_bound(_FwdIt _First, _FwdIt _Last, const _Ty% _Val);  
template<class _FwdIt, class _Ty, class _Pr> inline  
    _FwdIt lower_bound(_FwdIt _First, _FwdIt _Last,  
        const _Ty% _Val, _Pr _Pred);  
```  
  
## Remarks  
 This function behaves the same as the STL function `lower_bound`. For more information, see [lower_bound](../vs140/lower_bound.md).  
  
## Requirements  
 **Header:** <cliext/algorithm>  
  
 **Namespace:** cliext  
  
## See Also  
 [algorithm (STL/CLR)](../vs140/algorithm--STL-CLR-.md)