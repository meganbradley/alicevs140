---
title: "wait Function"
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
ms.assetid: a8a326d1-854d-4462-b705-36d3a2a6fb2b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# wait Function
Pauses the current context for a specified amount of time.  
  
## Syntax  
  
```  
void __cdecl wait(  
   unsigned int _Milliseconds  
);  
```  
  
#### Parameters  
 `_Milliseconds`  
 The number of milliseconds the current context should be paused for. If the `_Milliseconds` parameter is set to the value `0`, the current context should yield execution to other runnable contexts before continuing.  
  
## Remarks  
 If this method is called on a Concurrency Runtime scheduler context, the scheduler will find a different context to run on the underlying resource. Because the scheduler is cooperative in nature, this context cannot resume exactly after the number of milliseconds specified. If the scheduler is busy executing other tasks that do not cooperatively yield to the scheduler, the wait period could be indefinite.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)