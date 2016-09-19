---
title: "Termination and Detaching"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 268c1e51-6363-45d1-964c-1ab99bdfa4f9
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Termination and Detaching
The following describes normal termination.  
  
## Discussion  
 After the [IDebugLoadCompleteEvent2](../vs140/IDebugLoadCompleteEvent2.md) or [IDebugEntryPointEvent2](../vs140/IDebugEntryPointEvent2.md) interface continues, if there are no breakpoints, exceptions, run-time errors, or infinite loops in the application to be debugged, the program being debugged will run to completion. This is normal termination.  
  
 You must send an [IDebugProgramDestroyEvent2](../vs140/IDebugProgramDestroyEvent2.md) to implement normal termination. This requires implementing the [IDebugProgramDestroyEvent2::GetExitCode](../vs140/IDebugProgramDestroyEvent2--GetExitCode.md) method.  
  
## See Also  
 [Creating a Custom Debug Engine](../vs140/Creating-a-Custom-Debug-Engine.md)