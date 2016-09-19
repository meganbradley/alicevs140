---
title: "undeclare_reachable"
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
ms.assetid: 67f7845e-48a8-4531-a049-b6a4957bcaec
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# undeclare_reachable
Informs a `garbage_collector` that a specified memory location is not reachable.  
  
## Syntax  
  
```  
template<class Type>  
    Type *undeclare_reachable(Type *_Ptr);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Ptr`|A pointer to the memory address to be declared not reachable.|  
  
## Property Value/Return Value  
 Returns a pointer to the specified memory location.  
  
## Remarks  
 If `_Ptr` is not `null`, the function informs any `garbage collector` that `_Ptr` is hereafter not `reachable`. It returns a `safely derived` pointer that compares equal to `_Ptr`.  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [<memory\>](../vs140/-memory-.md)