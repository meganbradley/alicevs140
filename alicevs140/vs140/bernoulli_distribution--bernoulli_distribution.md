---
title: "bernoulli_distribution::bernoulli_distribution"
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
ms.assetid: 004524dc-fc9e-426f-b9e1-34525aa80c78
caps.latest.revision: 25
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# bernoulli_distribution::bernoulli_distribution
Constructs the distribution.  
  
## Syntax  
  
```  
explicit bernoulli_distribution(double p = 0.5);  
  
explicit bernoulli_distribution(const param_type& parm);  
```  
  
#### Parameters  
 `p`  
 The stored `p` distribution parameter.  
  
 `parm`  
 The parameter structure used to construct the distribution.  
  
## Remarks  
 **Precondition:** `0.0 ≤ p ≤ 1.0`  
  
 The first constructor constructs an object whose stored `p` value holds the value `p`.  
  
 The second constructor constructs an object whose stored parameters are initialized from `parm`. You can obtain and set the current parameters of an existing distribution by calling the `param()` member function.  
  
 For more information and a code example, see [bernoulli_distribution Class](../vs140/binomial_distribution-Class.md).  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)   
 [bernoulli_distribution Class](../vs140/bernoulli_distribution-Class.md)