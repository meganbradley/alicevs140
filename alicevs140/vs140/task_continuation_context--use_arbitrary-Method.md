---
title: "task_continuation_context::use_arbitrary Method"
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
ms.assetid: 6b548316-fb12-4390-a5d6-0f7e14e0ccaa
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# task_continuation_context::use_arbitrary Method
Creates a task continuation context which allows the Runtime to choose the execution context for a continuation.  
  
## Syntax  
  
```  
static task_continuation_context use_arbitrary();  
```  
  
## Return Value  
 A task continuation context that represents an arbitrary location.  
  
## Remarks  
 When this continuation context is used the continuation will execute in a context the runtime chooses even if the antecedent task is apartment aware.  
  
 `use_arbitrary` can be used to turn off the default behavior for a continuation on an apartment aware task created in an STA.  
  
 This method is only available to Windows Store apps.  
  
## Requirements  
 **Header:** ppltasks.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [task_continuation_context Class](../vs140/task_continuation_context-Class.md)