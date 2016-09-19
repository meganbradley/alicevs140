---
title: "student_t_distribution::student_t_distribution"
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
ms.assetid: c8f1a27e-1127-4df9-9a66-0cadf1cbb553
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# student_t_distribution::student_t_distribution
Constructs the distribution.  
  
## Syntax  
  
```  
explicit student_t_distribution(RealType n = 1.0);  
  
explicit student_t_distribution(const param_type& parm);  
```  
  
#### Parameters  
 `n`  
 The `n` distribution parameter.  
  
 `parm`  
 The parameter package used to construct the distribution.  
  
## Remarks  
 **Precondition:** `0.0 < n`  
  
 The first constructor constructs an object whose stored `n` value holds the value `n`.  
  
 The second constructor constructs an object whose stored parameters are initialized from `parm`. You can obtain and set the current parameters of an existing distribution by calling the `param()` member function.  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)   
 [student_t_distribution Class](../vs140/student_t_distribution-Class.md)