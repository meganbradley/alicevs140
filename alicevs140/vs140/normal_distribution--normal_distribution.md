---
title: "normal_distribution::normal_distribution"
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
ms.assetid: 68a687e3-6e48-4fa3-af30-dbcec28e6123
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# normal_distribution::normal_distribution
Constructs the distribution.  
  
## Syntax  
  
```  
explicit normal_distribution(RealType mean = 0.0, RealType stddev = 1.0);  
  
explicit normal_distribution(const param_type& parm);  
```  
  
#### Parameters  
 `mean`  
 The `mean` distribution parameter.  
  
 `stddev`  
 The `stddev` distribution parameter.  
  
 `parm`  
 The parameter structure used to construct the distribution.  
  
## Remarks  
 **Precondition:** `0.0 ≤ stddev`  
  
 The first constructor constructs an object whose stored `mean` value holds the value `mean` and whose stored `stddev` value holds the value `stddev`.  
  
 The second constructor constructs an object whose stored parameters are initialized from `parm`. You can obtain and set the current parameters of an existing distribution by calling the `param()` member function.  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)   
 [normal_distribution Class](../vs140/normal_distribution-Class.md)