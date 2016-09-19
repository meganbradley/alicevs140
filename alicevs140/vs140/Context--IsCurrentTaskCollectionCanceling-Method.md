---
title: "Context::IsCurrentTaskCollectionCanceling Method"
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
ms.assetid: 0188833b-7755-470c-8fd2-67de431eb2b4
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Context::IsCurrentTaskCollectionCanceling Method
Returns an indication of whether the task collection which is currently executing inline on the current context is in the midst of an active cancellation (or will be shortly).  
  
## Syntax  
  
```  
static bool __cdecl IsCurrentTaskCollectionCanceling();  
```  
  
## Return Value  
 If a scheduler is attached to the calling context and a task group is executing a task inline on that context, an indication of whether that task group is in the midst of an active cancellation (or will be shortly); otherwise, the value `false`.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Context Class](../vs140/Context-Class.md)