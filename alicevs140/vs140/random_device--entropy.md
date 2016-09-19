---
title: "random_device::entropy"
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
ms.assetid: 9a177aa9-bd70-42df-8034-3fc1d100c4af
caps.latest.revision: 20
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# random_device::entropy
Estimates the randomness of the source.  
  
## Syntax  
  
```  
double entropy() const noexcept;  
```  
  
## Remarks  
 The member function returns an estimate of the randomness of the source, as measured in bits.  
  
 For example code, see [random_device](../vs140/random_device-Class.md).  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)   
 [random_device](../vs140/random_device-Class.md)