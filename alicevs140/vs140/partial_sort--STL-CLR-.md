---
title: "partial_sort (STL-CLR)"
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
H1: partial_sort (STL/CLR)
ms.assetid: 5a73b275-aef0-4bda-8ae3-7c1196fe49c4
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# partial_sort (STL-CLR)
Arranges a specified number of the smaller elements in a range into a nondescending order or according to an ordering criterion specified by a binary predicate.  
  
## Syntax  
  
```  
template<class _RanIt> inline  
    void partial_sort(_RanIt _First, _RanIt _Mid, _RanIt _Last);  
template<class _RanIt, class _Pr> inline  
    void partial_sort(_RanIt _First, _RanIt _Mid, _RanIt _Last,  
        _Pr _Pred);  
```  
  
## Remarks  
 This function behaves the same as the STL function `partial_sort`. For more information, see [partial_sort](../vs140/partial_sort.md).  
  
## Requirements  
 **Header:** <cliext/algorithm>  
  
 **Namespace:** cliext  
  
## See Also  
 [algorithm (STL/CLR)](../vs140/algorithm--STL-CLR-.md)