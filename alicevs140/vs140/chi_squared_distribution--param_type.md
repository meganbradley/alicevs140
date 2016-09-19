---
title: "chi_squared_distribution::param_type"
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
ms.assetid: 2424b02f-18f5-459c-a688-34e1688c2241
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# chi_squared_distribution::param_type
Stores the parameters of the distribution.  
  
## Syntax  
  
```  
struct param_type {  
    typedef chi_squared_distribution<RealType> distribution_type;  
    param_type(RealType n = 1.0);  
    RealType n() const;  
    .....  
    bool operator==(const param_type& right) const;  
    bool operator!=(const param_type& right) const;  
    };  
```  
  
#### Parameters  
 See parent topic [chi_squared_distribution Class](../vs140/chi_squared_distribution-Class.md).  
  
## Remarks  
 **Precondition:** `0.0 < n`  
  
 This structure can be passed to the distribution's class constructor at instantiation, to the `param()` member function to set the stored parameters of an existing distribution, and to `operator()` to be used in place of the stored parameters.  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)   
 [chi_squared_distribution Class](../vs140/chi_squared_distribution-Class.md)