---
title: "valarray::swap"
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
ms.assetid: 261a6b2d-96a9-4fa3-87ec-d6be7e131eed
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# valarray::swap
Exchanges the elements of two `valarray`s.  
  
## Syntax  
  
```  
void swap(valarray& _Right);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Right`|A `valarray` providing the elements to be swapped.|  
  
## Remarks  
 The member function swaps the controlled sequences between `*this` and `_Right`. It does so in constant time, it throws no exceptions, and it invalidates no references, pointers, or iterators that designate elements in the two controlled sequences.  
  
## Requirements  
 **Header:** <valarray\>  
  
 **Namespace:** std  
  
## See Also  
 [valarray Class](../vs140/valarray-Class.md)   
 [<valarray\>](../vs140/-valarray-.md)