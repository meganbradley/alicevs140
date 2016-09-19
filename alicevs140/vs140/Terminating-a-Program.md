---
title: "Terminating a Program"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eedda0a3-5e05-44fe-841d-a2f4866ac72d
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Terminating a Program
The following is a description of the termination of a single program with one thread.  
  
## Termination Process  
  
1.  The DE sends an [IDebugThreadDestroyEvent2](../vs140/IDebugThreadDestroyEvent2.md) with a valid [IDebugThread2](../vs140/IDebugThread2.md).  
  
2.  The DE sends an [IDebugProgramDestroyEvent2](../vs140/IDebugProgramDestroyEvent2.md) with a valid [IDebugProgram2](../vs140/IDebugProgram2.md).  
  
 The IDE goes into design mode. The debug engine or run-time environment calls [IDebugPortNotify2::RemoveProgramNode](../vs140/IDebugPortNotify2--RemoveProgramNode.md) to remove the program from the port.  
  
## See Also  
 [Calling Debugger Events](../vs140/Calling-Debugger-Events.md)