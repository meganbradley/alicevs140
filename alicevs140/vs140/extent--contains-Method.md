---
title: "extent::contains Method"
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
ms.assetid: 28b6094f-ffcf-4c7f-b968-40e5c8c77961
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# extent::contains Method
Indicates whether the specified [index](../vs140/index-Class.md) value is contained within the [extent](../vs140/extent-Class--C---AMP-.md) object.  
  
## Syntax  
  
```  
bool contains(  
   const index<rank>& _Index  
) const restrict(amp,cpu);  
```  
  
#### Parameters  
 `_Index`  
 The `index` value to test.  
  
## Return Value  
 `true` if the specified `index` value is contained in the `extent` object; otherwise, `false`.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [extent Class  (C++ Accelerated Massive Parallelism)](../vs140/extent-Class--C---AMP-.md)