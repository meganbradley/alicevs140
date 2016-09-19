---
title: "sampler::get_filter_mode Method"
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
ms.assetid: f3cdce91-c563-4b1f-8be9-247b1a12c0fa
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# sampler::get_filter_mode Method
Returns the filter mode that’s configured for this `sampler`.  
  
## Syntax  
  
```  
Concurrency::graphics::filter_mode get_filter_mode() const restrict(amp, cpu);  
```  
  
## Return Value  
 The filter mode that’s configured for the sampler.  
  
## Remarks  
 The same filter mode applies to the minimization, maximization, and mipmap filters.  
  
## Requirements  
 **Header:** amp_graphics.h  
  
 **Namespace:** concurrency::graphics  
  
## See Also  
 [sampler Class](../vs140/sampler-Class.md)