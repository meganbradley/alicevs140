---
title: "array_view::synchronize Method"
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
ms.assetid: 124cc736-d511-42cb-8e2b-17bb75a6c2de
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# array_view::synchronize Method
Synchronizes any modifications made to the `array_view` object back to its source data.  
  
## Syntax  
  
```  
void synchronize(  
   access_type _Access_type = access_type_read  
) const restrict(cpu);  
  
void synchronize() const restrict(cpu);  
```  
  
#### Parameters  
 `_Access_type`  
 The intended [access_type](../vs140/access_type-Enumeration.md) on the target [accelerator_view](../vs140/accelerator_view-Class.md). This parameter has a default value of `access_type_read`.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [array_view Class](../vs140/array_view-Class.md)