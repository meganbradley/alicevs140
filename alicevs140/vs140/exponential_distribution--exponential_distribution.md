---
title: "exponential_distribution::exponential_distribution"
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
ms.assetid: 1444d2b4-b00f-45aa-b27b-3f536310676f
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# exponential_distribution::exponential_distribution
Constructs the distribution.  
  
## Syntax  
  
```  
explicit exponential_distribution(RealType lambda = 1.0);  
  
explicit exponential_distribution(const param_type& parm);  
```  
  
#### Parameters  
 `lambda`  
 The `lambda` distribution parameter.  
  
 `parm`  
 The parameter package used to construct the distribution.  
  
## Remarks  
 **Precondition:** `0.0 < lambda`  
  
 The first constructor constructs an object whose stored `lambda` value holds the value `lambda`.  
  
 The second constructor constructs an object whose stored parameters are initialized from `parm`. You can obtain and set the current parameters of an existing distribution by calling the `param()` member function.  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)   
 [exponential_distribution Class](../vs140/exponential_distribution-Class.md)