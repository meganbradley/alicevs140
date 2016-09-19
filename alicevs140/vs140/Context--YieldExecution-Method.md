---
title: "Context::YieldExecution Method"
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
ms.assetid: e92707b3-0e23-4e78-af3d-4eeb34bf5709
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Context::YieldExecution Method
Yields execution so that another context can execute. If no other context is available to yield to, the scheduler can yield to another operating system thread.  
  
## Syntax  
  
```  
static void __cdecl YieldExecution();  
```  
  
## Remarks  
 This method will result in the process' default scheduler being created and/or attached to the calling context if there is no scheduler currently associated with the calling context.  
  
 This function is new in [!INCLUDE[vs_dev14](../vs140/includes/vs_dev14_md.md)] and is identical to the [Yield](../vs140/Context--Yield-Method.md) function but does not conflict with the Yield macro in Windows.h.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Context Class](../vs140/Context-Class.md)   
 [Context::Block Method](../vs140/Context--Block-Method.md)   
 [Context::Unblock Method](../vs140/Context--Unblock-Method.md)