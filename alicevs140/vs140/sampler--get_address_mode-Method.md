---
title: "sampler::get_address_mode Method"
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
ms.assetid: 918966c7-8c07-4710-a2f4-8bc249ef0fd9
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# sampler::get_address_mode Method
Returns the filter mode that’s configured for this `sampler`.  
  
## Syntax  
  
```  
Concurrency::graphics::address_mode get_address_mode() const __GPU;  
```  
  
## Return Value  
 The address mode that’s configured for the sampler.  
  
## Remarks  
 The same address mode applies to all dimensions.  
  
## Requirements  
 **Header:** amp_graphics.h  
  
 **Namespace:** concurrency::graphics  
  
## See Also  
 [sampler Class](../vs140/sampler-Class.md)