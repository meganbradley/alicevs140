---
title: "unique_lock::swap Method"
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
ms.assetid: 50d6f79a-009b-44b8-8721-4b1c13bc67e9
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unique_lock::swap Method
Swaps the associated `mutex` and ownership status with that of a specified object.  
  
## Syntax  
  
```  
void swap(  
   unique_lock& Other  
) _NOEXCEPT;  
```  
  
#### Parameters  
 `Other`  
 A `unique_lock` object.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [unique_lock Class](../vs140/unique_lock-Class.md)   
 [<mutex\>](../vs140/-mutex-.md)