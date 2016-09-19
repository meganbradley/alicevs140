---
title: "Attaching and Detaching to a Program"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 79dcbb9b-c7f8-40fc-8a00-f37fe1934f51
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Attaching and Detaching to a Program
Attaching the debugger requires sending the correct sequence of methods and events with the proper attributes.  
  
## Sequence of Methods and Events  
  
1.  The session debug manager (SDM) calls the [IDebugProgramNodeAttach2::OnAttach](../vs140/IDebugProgramNodeAttach2--OnAttach.md) method.  
  
     Based on the debug engine (DE) process model, the `IDebugProgramNodeAttach2::OnAttach` method returns one of the following methods, which determines what happens next.  
  
     If `S_FALSE` is returned, the debug engine has successfully been attached to the program. Otherwise, the [Attach](../vs140/IDebugEngine2--Attach.md) method is called to complete the attach process.  
  
     If `S_OK` is returned, the DE is to be loaded in the same process as the SDM. The SDM performs the following tasks:  
  
    1.  Calls [GetEngineInfo](../vs140/IDebugProgramNode2--GetEngineInfo.md) to get the engine information of the DE.  
  
    2.  Co-creates the DE.  
  
    3.  Calls [Attach](../vs140/IDebugEngine2--Attach.md).  
  
2.  The DE sends an [IDebugEngineCreateEvent2](../vs140/IDebugEngineCreateEvent2.md) to the SDM with an `EVENT_SYNC` attribute.  
  
3.  The DE sends an [IDebugProgramCreateEvent2](../vs140/IDebugProgramCreateEvent2.md) to the SDM with an `EVENT_SYNC` attribute.  
  
4.  The DE sends an [IDebugLoadCompleteEvent2](../vs140/IDebugLoadCompleteEvent2.md) to the SDM with an `EVENT_SYNC_STOP` attribute.  
  
 Detaching from a program is a simple, two-step process, as follows:  
  
1.  The SDM calls [Detach](../vs140/IDebugProgram2--Detach.md).  
  
2.  The DE sends an [IDebugProgramDestroyEvent2](../vs140/IDebugProgramDestroyEvent2.md).  
  
## See Also  
 [Calling Debugger Events](../vs140/Calling-Debugger-Events.md)