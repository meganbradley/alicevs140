---
title: "SetNotificationForWaitCompletion Method"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: da149c9a-20f4-4543-a29e-429c8c1d2e19
caps.latest.revision: 7
translation.priority.mt: 
  - de-de
  - ja-jp
---
# SetNotificationForWaitCompletion Method
Sets or clears the TASK_STATE_WAIT_COMPLETION_NOTIFICATION state bit.  
  
 **Namespace:** <xref:System.Threading.Tasks?qualifyHint=True>  
  
 **Assembly:** mscorlib (in mscorlib.dll)  
  
## Syntax  
  
```vb  
internal void SetNotificationForWaitCompletion(bool enabled)  
```  
  
#### Parameters  
 `enabled`  
  
 `true` to set the bit; `false` to unset the bit.  
  
## Exceptions  
  
## Remarks  
 The debugger sets this bit to help step out of an async method body. If `enabled` is `true`, this method must be called only on a task that has not yet been completed. If `enabled` is `false`, this method may be called on completed tasks. In either event, it should only be used for promise-style tasks.  
  
## Requirements  
  
## See Also  
 [Task Class - Internal Members](../Topic/Task%20Class%20-%20Internal%20Members.md)