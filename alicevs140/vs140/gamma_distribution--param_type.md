---
title: "gamma_distribution::param_type"
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
ms.assetid: 2b7e37c2-3102-4ed9-ba60-b0d96a645d2b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# gamma_distribution::param_type
Stores the parameters of the distribution.  
  
## Syntax  
  
```  
struct param_type {  
    typedef gamma_distribution<RealType> distribution_type;  
    param_type(RealType alpha = 1.0, RealType beta 1.0);  
    RealType alpha() const;  
    RealType beta() const;  
    .....  
    bool operator==(const param_type& right) const;  
    bool operator!=(const param_type& right) const;  
};  
```  
  
#### Parameters  
 See parent topic [gamma_distribution Class](../vs140/gamma_distribution-Class.md).  
  
## Remarks  
 **Precondition:** `0.0 < alpha` and `0.0 < beta`  
  
 This structure can be passed to the distribution's class constructor at instantiation, to the `param()` member function to set the stored parameters of an existing distribution, and to `operator()` to be used in place of the stored parameters.  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)   
 [gamma_distribution Class](../vs140/gamma_distribution-Class.md)