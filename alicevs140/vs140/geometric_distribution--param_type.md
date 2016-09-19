---
title: "geometric_distribution::param_type"
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
ms.assetid: bdc78cef-8794-45f3-b02b-f3394841b7bc
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# geometric_distribution::param_type
Stores the parameters of the distribution.  
  
## Syntax  
  
```  
struct param_type {  
    typedef geometric_distribution<IntType, RealType> distribution_type;  
    param_type(RealType p = 0.5);  
    RealType p() const;  
    .....  
    bool operator==(const param_type& right) const;  
    bool operator!=(const param_type& right) const;  
};  
```  
  
#### Parameters  
 See parent topic [geometric_distribution Class](../vs140/geometric_distribution-Class.md).  
  
## Remarks  
 **Precondition:** `0.0 < p && p < 1.0`  
  
 This structure can be passed to the distribution's class constructor at instantiation, to the `param()` member function to set the stored parameters of an existing distribution, and to `operator()` to be used in place of the stored parameters.  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)   
 [geometric_distribution Class](../vs140/geometric_distribution-Class.md)