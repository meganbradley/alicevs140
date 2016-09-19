---
title: "Context::Yield Method"
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
ms.assetid: 5759ad0a-b97a-4f86-8015-cd8d40256383
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Context::Yield Method
Yields execution so that another context can execute. If no other context is available to yield to, the scheduler can yield to another operating system thread.  
  
## Syntax  
  
```  
static void __cdecl Yield();  
```  
  
## Remarks  
 This method will result in the process' default scheduler being created and/or attached to the calling context if there is no scheduler currently associated with the calling context.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Context Class](../vs140/Context-Class.md)   
 [Context::Block Method](../vs140/Context--Block-Method.md)   
 [Context::Unblock Method](../vs140/Context--Unblock-Method.md)