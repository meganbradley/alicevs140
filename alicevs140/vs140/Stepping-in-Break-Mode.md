---
title: "Stepping in Break Mode"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b08dc8ee-6c63-4462-a097-6f525cfbb35a
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Stepping in Break Mode
The following describes the process that occurs when the debugger is in break mode and must step through code:  
  
## Stepping Process  
  
1.  Call [IDebugProgram2::Step](../vs140/IDebugProgram2--Step.md) with [STEPKIND](../vs140/STEPKIND.md) and [STEPUNIT](../vs140/STEPUNIT.md) arguments to execute a step.  
  
2.  When the step is finished, send an [IDebugStepCompleteEvent2](../vs140/IDebugStepCompleteEvent2.md) as a stopping event.  
  
## See Also  
 [Calling Debugger Events](../vs140/Calling-Debugger-Events.md)