---
title: "TASK_STATE_WAITING_ON_CHILDREN Field"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6f26b098-84ad-4f6e-ba27-6136581ba630
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# TASK_STATE_WAITING_ON_CHILDREN Field
The task has finished executing its delegate and is implicitly waiting for attached child tasks to complete.  
  
 **Namespace:** <xref:System.Threading.Tasks?qualifyHint=True>  
  
 **Assembly:** mscorlib (in mscorlib.dll)  
  
 Because you cannot access this internal member from the .NET Framework, the following syntax is provided in Common Intermediate Language (CIL).  
  
## Syntax  
  
```  
.field static assembly literal int32 TASK_STATE_WAITING_ON_CHILDREN = int32(0x01000000)  
```  
  
## Remarks  
 If the [m_stateFlags](../Topic/m_stateFlags%20Field.md) field contains this value, the <xref:System.Threading.Tasks.Task.Status?qualifyHint=False> property returns <xref:System.Threading.Tasks.TaskStatus.WaitingForChildrenToComplete?qualifyHint=True>.  
  
## See Also  
 [Task Class (Internals)](../Topic/Task%20Class%20-%20Internal%20Members.md)