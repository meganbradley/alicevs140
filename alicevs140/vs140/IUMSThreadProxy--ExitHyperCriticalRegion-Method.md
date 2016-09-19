---
title: "IUMSThreadProxy::ExitHyperCriticalRegion Method"
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
ms.assetid: 78259765-a74a-498f-84f3-903fd9c585c8
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IUMSThreadProxy::ExitHyperCriticalRegion Method
Called in order to exit a hyper-critical region.  
  
## Syntax  
  
```  
virtual int ExitHyperCriticalRegion() =0;  
```  
  
## Return Value  
 The new depth of hyper-critical region. Hyper-critical regions are reentrant.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [IUMSThreadProxy Structure](../vs140/IUMSThreadProxy-Structure.md)   
 [IUMSThreadProxy::EnterHyperCriticalRegion Method](../vs140/IUMSThreadProxy--EnterHyperCriticalRegion-Method.md)