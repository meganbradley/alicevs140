---
title: "IDebugStopCompleteEvent2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ff3e89f4-61bb-489d-901c-447260100218
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugStopCompleteEvent2
The debug engine (DE) can send this optional event to the session debug manager (SDM) when a program has stopped.  
  
## Syntax  
  
```  
IDebugStopCompleteEvent2 : IUnknown  
```  
  
## Notes for Implementers  
 This is a new interface for [!INCLUDE[vsprvslong](../vs140/includes/vsprvslong_md.md)]. Prior releases did not support asynchronous stopping.  
  
 [IDebugEngineProgram2::Stop](../vs140/IDebugEngineProgram2--Stop.md) is called by the SDM in multi-process or multi-program scenarios. When one program sends a stopping event to the SDM, the SDM requests other programs to stop, too.  
  
 It is used to asynchronously inform the SDM that a program has stopped. This is useful for an interpreter debug engine, where sometimes no code is running inside the debugged program, so [IDebugEngineProgram2::Stop](../vs140/IDebugEngineProgram2--Stop.md) can not be completed synchronously. If a debug engine wants to employ this asynchronous notification, it must return `S_ASYNC_STOP` from [IDebugEngineProgram2::Stop](../vs140/IDebugEngineProgram2--Stop.md).  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll