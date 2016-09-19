---
title: "negative_binomial_distribution::param_type"
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
ms.assetid: 236b784e-fea1-4e31-8b3c-40977d209cef
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# negative_binomial_distribution::param_type
Stores the parameters of the distribution.  
  
## Syntax  
  
```  
struct param_type {  
    typedef negative_binomial_distribution<IntType> distribution_type;  
    param_type(IntType k = 1, double p = 0.5);  
    IntType k() const;  
    double p() const;    .....  
    bool operator==(const param_type& right) const;  
    bool operator!=(const param_type& right) const;  
};  
```  
  
#### Parameters  
 See parent topic [negative_binomial_distribution Class](../vs140/negative_binomial_distribution-Class.md).  
  
## Remarks  
 **Precondition:** `0.0 < k` and `0.0 < p ≤ 1.0`  
  
 This structure can be passed to the distribution's class constructor at instantiation, to the `param()` member function to set the stored parameters of an existing distribution, and to `operator()` to be used in place of the stored parameters.  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)   
 [negative_binomial_distribution Class](../vs140/negative_binomial_distribution-Class.md)