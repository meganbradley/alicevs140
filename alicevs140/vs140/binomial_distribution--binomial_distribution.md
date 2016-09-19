---
title: "binomial_distribution::binomial_distribution"
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
ms.assetid: 738ca50b-baa0-4b19-90b7-b2ea39cd474a
caps.latest.revision: 25
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# binomial_distribution::binomial_distribution
Constructs the distribution.  
  
## Syntax  
  
```  
explicit binomial_distribution(IntType t = 1, double p = 0.5);  
  
explicit binomial_distribution(const param_type& parm);  
```  
  
#### Parameters  
 `t`  
 The `t` distribution parameter.  
  
 `p`  
 The `p` distribution parameter.  
  
 `parm`  
 The parameter structure used to construct the distribution.  
  
## Remarks  
 **Precondition:** `0 ≤ t` and `0.0 ≤ p ≤ 1.0`  
  
 The first constructor constructs an object whose stored `p` value holds the value `p` and whose stored `t` value holds the value `t`.  
  
 The second constructor constructs an object whose stored parameters are initialized from `parm`. You can obtain and set the current parameters of an existing distribution by calling the `param()` member function.  
  
 For more information and a code example, see [binomial_distribution Class](../vs140/binomial_distribution-Class.md).  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)   
 [binomial_distribution Class](../vs140/binomial_distribution-Class.md)