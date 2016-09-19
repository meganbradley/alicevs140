---
title: "copy (STL-CLR)"
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
H1: copy (STL/CLR)
ms.assetid: f6738535-fde6-446e-a797-bf2b457c2bff
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# copy (STL-CLR)
Assigns the values of elements from a source range to a destination range, iterating through the source sequence of elements and assigning them new positions in a forward direction.  
  
## Syntax  
  
```  
template<class _InIt, class _OutIt> inline  
    _OutIt copy(_InIt _First, _InIt _Last, _OutIt _Dest);  
```  
  
## Remarks  
 This function behaves the same as the STL function `copy`. For more information, see [copy](../vs140/copy.md).  
  
## Requirements  
 **Header:** <cliext/algorithm>  
  
 **Namespace:** cliext  
  
## See Also  
 [algorithm (STL/CLR)](../vs140/algorithm--STL-CLR-.md)