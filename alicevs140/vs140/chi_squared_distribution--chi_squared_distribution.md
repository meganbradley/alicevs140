---
title: "chi_squared_distribution::chi_squared_distribution"
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
ms.assetid: 0decc7af-c655-4b7c-859e-91e382888a3a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# chi_squared_distribution::chi_squared_distribution
Constructs the distribution.  
  
## Syntax  
  
```  
explicit chi_squared_distribution(RealType n = 1.0);  
  
explicit chi_squared_distribution(const param_type& parm);  
```  
  
#### Parameters  
 `n`  
 The `n` distribution parameter.  
  
 `parm`  
 The parameter structure used to construct the distribution.  
  
## Remarks  
 **Precondition:** `0.0 < n`  
  
 The first constructor constructs an object whose stored `n` value holds the value `n`.  
  
 The second constructor constructs an object whose stored parameters are initialized from `parm`. You can obtain and set the current parameters of an existing distribution by calling the `param()` member function.  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)   
 [chi_squared_distribution Class](../vs140/chi_squared_distribution-Class.md)