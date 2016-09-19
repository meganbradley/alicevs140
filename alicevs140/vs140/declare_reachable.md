---
title: "declare_reachable"
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
ms.assetid: 9a02670f-f8ca-4581-8f8b-f0510830d5a5
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# declare_reachable
Informs garbage collection that the indicated address is to allocated storage and is reachable.  
  
## Syntax  
  
```  
void declare_reachable(  
    void *_Ptr  
);  
```  
  
#### Parameters  
 `_Ptr`  
 A pointer to a reachable, allocated, valid storage area.  
  
## Remarks  
 If `_Ptr` is not null, the function informs any garbage collector that `_Ptr` is hereafter reachable (points to valid allocated storage).  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [<memory\>](../vs140/-memory-.md)