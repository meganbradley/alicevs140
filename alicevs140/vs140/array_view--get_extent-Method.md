---
title: "array_view::get_extent Method"
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
ms.assetid: 7998b599-501c-4c84-8610-ad280a88bb3f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# array_view::get_extent Method
Returns the [extent](../vs140/extent-Class--C---AMP-.md) object of the [array_view](../vs140/array_view-Class.md) object.  
  
## Syntax  
  
```  
Concurrency::extent<_Rank> get_extent() const restrict(cpu, amp);  
```  
  
## Return Value  
 The `extent` object of the `array_view` object  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [array_view Class](../vs140/array_view-Class.md)