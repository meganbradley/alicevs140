---
title: "TASK_STATE_CANCELED Field"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f4f5a96a-8230-493d-9696-8d2716bda261
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# TASK_STATE_CANCELED Field
The task was canceled before it reached the running state, or it acknowledged its cancellation and completed without exception.  
  
 **Namespace:** <xref:System.Threading.Tasks?qualifyHint=True>  
  
 **Assembly:** mscorlib (in mscorlib.dll)  
  
 Because you cannot access this internal member from the .NET Framework, the following syntax is provided in Common Intermediate Language (CIL).  
  
## Syntax  
  
```  
.field static assembly literal int32 TASK_STATE_CANCELED = int32(0x00800000)  
```  
  
## Remarks  
 If the [m_stateFlags](../Topic/m_stateFlags%20Field.md) field contains this value, the <xref:System.Threading.Tasks.Task.Status?qualifyHint=False> property returns <xref:System.Threading.Tasks.TaskStatus.Canceled?qualifyHint=True>.  
  
## See Also  
 [Task Class (Internals)](../Topic/Task%20Class%20-%20Internal%20Members.md)