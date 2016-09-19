---
title: "weibull_distribution::param_type"
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
ms.assetid: b8879017-2432-48e1-ae5b-4741a3c88c05
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# weibull_distribution::param_type
Stores the parameters of the distribution.  
  
## Syntax  
  
```  
struct param_type {  
    typedef weibull_distribution<RealType> distribution_type;  
    param_type(RealType a = 1.0, RealType b = 1.0);  
    RealType a() const;  
    RealType b() const;  
    .....  
    bool operator==(const param_type& right) const;  
    bool operator!=(const param_type& right) const;  
};  
```  
  
#### Parameters  
 See parent topic [weibull_distribution Class](../vs140/weibull_distribution-Class.md).  
  
## Remarks  
 **Precondition:** `0.0 < a` and `0.0 < b`  
  
 This structure can be passed to the distribution's class constructor at instantiation, to the `param()` member function to set the stored parameters of an existing distribution, and to `operator()` to be used in place of the stored parameters.  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)   
 [weibull_distribution Class](../vs140/weibull_distribution-Class.md)