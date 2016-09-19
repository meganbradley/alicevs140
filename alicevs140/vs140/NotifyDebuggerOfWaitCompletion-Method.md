---
title: "NotifyDebuggerOfWaitCompletion Method"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 841c5908-4f3f-400b-a7b0-96a95f362817
caps.latest.revision: 5
translation.priority.mt: 
  - de-de
  - ja-jp
---
# NotifyDebuggerOfWaitCompletion Method
Placeholder method used as a breakpoint target by the debugger. This method must not be inlined or optimized.  
  
 **Namespace:** <xref:System.Threading.Tasks?qualifyHint=True>  
  
 **Assembly:** mscorlib (in mscorlib.dll)  
  
## Syntax  
  
```vb  
private void NotifyDebuggerOfWaitCompletion()  
```  
  
## Remarks  
 All join operations with a task should call this method if their debugger notification bit is set.  
  
## Requirements  
  
## See Also  
 [Task Class - Internal Members](../Topic/Task%20Class%20-%20Internal%20Members.md)