---
title: "discrete_distribution::param_type"
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
ms.assetid: d665230c-36dc-403f-befe-e4f47b0908df
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# discrete_distribution::param_type
Stores all the parameters of the distribution.  
  
## Syntax  
  
```  
struct param_type {  
    typedef discrete_distribution<IntType> distribution_type;  
    param_type();  
    template<class UnaryOperation>  
    param_type(size_t count, double low, double high,         UnaryOperation weightfunc);  
    std::vector<double> probabilities() const;  
    ....  
    bool operator==(const param_type& right) const;  
    bool operator!=(const param_type& right) const;  
};  
```  
  
#### Parameters  
 See parent topic [discrete_distribution Class](../vs140/discrete_distribution-Class.md).  
  
## Remarks  
 This parameter package can be passed to [operator()](../vs140/discrete_distribution--operator--.md) to generate the return value.  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)   
 [discrete_distribution Class](../vs140/discrete_distribution-Class.md)