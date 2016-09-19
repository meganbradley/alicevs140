---
title: "random_device::operator()"
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
ms.assetid: ca5fc937-79b4-489d-a43c-3720fb87c9c7
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# random_device::operator()
Returns a random value.  
  
## Syntax  
  
```  
result_type operator()();  
```  
  
## Remarks  
 Returns values uniformly distributed in the closed interval [`min, max`] as determined by member functions `min()` and `max()`. Throws a value of an implementation-defined type derived from [exception](../vs140/exception-Class.md) if a random number could not be obtained.  
  
 For example code, see [random_device](../vs140/random_device-Class.md).  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)   
 [random_device](../vs140/random_device-Class.md)