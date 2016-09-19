---
title: "IUMSThreadProxy::GetCriticalRegionType Method"
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
ms.assetid: 6512c8e2-8db3-4f55-a6b0-b3b71946bf47
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IUMSThreadProxy::GetCriticalRegionType Method
Returns what kind of critical region the thread proxy is within. Because hyper-critical regions are a superset of critical regions, if code has entered a critical region and then a hyper-critical region, `InsideHyperCriticalRegion` will be returned.  
  
## Syntax  
  
```  
virtual CriticalRegionType GetCriticalRegionType() const =0;  
```  
  
## Return Value  
 The type of critical region the thread proxy is within.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [IUMSThreadProxy Structure](../vs140/IUMSThreadProxy-Structure.md)   
 [CriticalRegionType Enumeration](../vs140/CriticalRegionType-Enumeration.md)