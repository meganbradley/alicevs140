---
title: "accelerator::get_supports_limited_double_precision Method"
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
ms.assetid: 2fdb9c32-81b0-4224-9dab-4277be44ce75
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# accelerator::get_supports_limited_double_precision Method
Returns a Boolean value that indicates whether the accelerator has limited support for double precision math. If the accelerator has only limited support, then fused multiply add (FMA), division, reciprocal, and casting between `int` and `double` are not supported.  
  
## Syntax  
  
```  
bool get_supports_limited_double_precision() const;  
```  
  
## Return Value  
 `true` if the accelerator has limited support for double precision math; otherwise, `false`.  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [accelerator Class](../vs140/accelerator-Class.md)