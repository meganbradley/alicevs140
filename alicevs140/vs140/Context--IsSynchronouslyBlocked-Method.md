---
title: "Context::IsSynchronouslyBlocked Method"
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
ms.assetid: c2b6336e-0e36-40be-a03e-1806eafe470a
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Context::IsSynchronouslyBlocked Method
Determines whether or not the context is synchronously blocked. A context is considered to be synchronously blocked if it explicitly performed an action which led to blocking.  
  
## Syntax  
  
```  
virtual bool IsSynchronouslyBlocked() const =0;  
```  
  
## Return Value  
 Whether the context is synchronously blocked.  
  
## Remarks  
 A context is considered to be synchronously blocked if it explicitly performed an action which led to blocking. On the thread scheduler, this would indicate a direct call to the `Context::Block` method or a synchronization object which was built using the `Context::Block` method.  
  
 The return value from this method is an instantaneous sample of whether the context is synchronously blocked. This value may be stale the moment it is returned and can only be used under very specific circumstances.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Context Class](../vs140/Context-Class.md)   
 [Context::Block Method](../vs140/Context--Block-Method.md)