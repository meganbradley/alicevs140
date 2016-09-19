---
title: "IUMSThreadProxy::ExitCriticalRegion Method"
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
ms.assetid: 29911d4c-eaff-4909-b34b-bd3ebfc8b3ce
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IUMSThreadProxy::ExitCriticalRegion Method
Called in order to exit a critical region.  
  
## Syntax  
  
```  
virtual int ExitCriticalRegion() =0;  
```  
  
## Return Value  
 The new depth of critical region. Critical regions are reentrant.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [IUMSThreadProxy Structure](../vs140/IUMSThreadProxy-Structure.md)   
 [IUMSThreadProxy::EnterCriticalRegion Method](../vs140/IUMSThreadProxy--EnterCriticalRegion-Method.md)