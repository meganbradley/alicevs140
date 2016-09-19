---
title: "Supported Event Types"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a3c0386d-551e-4734-9a0c-368d1c2e6671
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Supported Event Types
Visual Studio debugging currently supports the following event types:  
  
-   Asynchronous events  
  
     Notify the session debug manager (SDM) and IDE that the state of the application being debugged is changing. These events are processed at the leisure of the SDM and the IDE. No reply is sent to the debug engine (DE) once the event is processed. The [IDebugOutputStringEvent2](../vs140/IDebugOutputStringEvent2.md) and [IDebugMessageEvent2](../vs140/IDebugMessageEvent2.md) interfaces are examples of asynchronous events.  
  
-   Synchronous events  
  
     Notify the SDM and IDE that the state of the application being debugged is changing. The only difference between these events and asynchronous events is that a reply is sent by means of the [ContinueFromSynchronousEvent](../vs140/IDebugEngine2--ContinueFromSynchronousEvent.md) method.  
  
     Sending a synchronous event is useful if you need your DE to continue processing after the IDE receives and processes the event.  
  
-   Synchronous stopping events, or stopping events  
  
     Notify the SDM and the IDE that the application being debugged has stopped executing code. When you send a stopping event by means of the method [IDebugEventCallback2::Event](../vs140/IDebugEventCallback2--Event.md), the [IDebugThread2](../vs140/IDebugThread2.md) parameter is required. Stopping events are continued by a call to the one of the following methods:  
  
    -   [Execute](../vs140/IDebugProgram2--Execute.md)  
  
    -   [Step](../vs140/IDebugProgram2--Step.md)  
  
    -   [Continue](../vs140/IDebugProgram2--Continue.md)  
  
     The interfaces [IDebugBreakpointEvent2](../vs140/IDebugBreakpointEvent2.md) and [IDebugExceptionEvent2](../vs140/IDebugExceptionEvent2.md) are examples of stopping events.  
  
    > [!NOTE]
    >  Asynchronous stopping events are not supported. It is an error to send an asynchronous stopping event.  
  
## Discussion  
 The actual implementation of events depends on the design of your DE. The type of each event sent is determined by its attributes, which are set when you design the DE. For example, one DE may send an [IDebugProgramCreateEvent2](../vs140/IDebugProgramCreateEvent2.md) as an asynchronous event, while another may send it as a stopping event.  
  
 The following table specifies which program and thread parameters are required for which events, as well as event types. Any event can be synchronous. No event needs to be synchronous.  
  
> [!NOTE]
>  The [IDebugEngine2](../vs140/IDebugEngine2.md) interface is required for all events.  
  
|Event|IDebugProgram2|IDebugThread2|Stopping Events|  
|-----------|--------------------|-------------------|---------------------|  
|[IDebugActivateDocumentEvent2](../vs140/IDebugActivateDocumentEvent2.md)|Allowed, but not required|Allowed, but not required|No|  
|[IDebugBreakEvent2](../vs140/IDebugBreakEvent2.md)|Required|Required|Yes|  
|[IDebugBreakpointBoundEvent2](../vs140/IDebugBreakpointBoundEvent2.md)|Allowed, but not required|Allowed, but not required|No|  
|[IDebugBreakpointErrorEvent2](../vs140/IDebugBreakpointErrorEvent2.md)|Allowed, but not required|Allowed, but not required|No|  
|[IDebugBreakpointUnboundEvent2](../vs140/IDebugBreakpointUnboundEvent2.md)|Allowed, but not required|Allowed, but not required|No|  
|[IDebugBreakpointEvent2](../vs140/IDebugBreakpointEvent2.md)|Required|Required|Yes|  
|[IDebugCanStopEvent2](../vs140/IDebugCanStopEvent2.md)|Required|Required|No|  
|[IDebugDocumentTextEvents2](../Topic/IDebugDocumentTextEvents2.md)|Not allowed|Not allowed|No|  
|[IDebugEngineCreateEvent2](../vs140/IDebugEngineCreateEvent2.md)|Not allowed|Not allowed|No|  
|[IDebugEntryPointEvent2](../vs140/IDebugEntryPointEvent2.md)|Required|Required|Yes|  
|[IDebugErrorEvent2](../vs140/IDebugErrorEvent2.md)|Allowed, but not required|Allowed, but not required|Can be|  
|[IDebugExceptionEvent2](../vs140/IDebugExceptionEvent2.md)|Required|Required|Yes|  
|[IDebugExpressionEvaluationCompleteEvent2](../vs140/IDebugExpressionEvaluationCompleteEvent2.md)|Allowed, but not required|Allowed, but not required|Can be|  
|[IDebugInterceptExceptionCompleteEvent2](../vs140/IDebugInterceptExceptionCompleteEvent2.md)|Required|Required|Yes|  
|[IDebugLoadCompleteEvent2](../vs140/IDebugLoadCompleteEvent2.md)|Required|Required|Yes|  
|[IDebugMessageEvent2](../vs140/IDebugMessageEvent2.md)|Allowed, but not required|Allowed, but not required|Can be|  
|[IDebugModuleLoadEvent2](../vs140/IDebugModuleLoadEvent2.md)|Required|Allowed, but not required|No|  
|[IDebugOutputStringEvent2](../vs140/IDebugOutputStringEvent2.md)|Allowed, but not required|Allowed, but not required|No|  
|[IDebugProgramCreateEvent2](../vs140/IDebugProgramCreateEvent2.md)|Required|Allowed, but not required|No|  
|[IDebugProgramDestroyEvent2](../vs140/IDebugProgramDestroyEvent2.md)|Required|Allowed, but not required|No|  
|[IDebugPropertyCreateEvent2](../vs140/IDebugPropertyCreateEvent2.md)|Required|Allowed, but not required|No|  
|[IDebugPropertyDestroyEvent2](../vs140/IDebugPropertyDestroyEvent2.md)|Required|Allowed, but not required|No|  
|[IDebugReturnValueEvent2](../vs140/IDebugReturnValueEvent2.md)|Allowed, but not required|Allowed, but not required|No|  
|IDebugStopCompleteEvent2|Required|Required|Yes|  
|[IDebugStepCompleteEvent2](../vs140/IDebugStepCompleteEvent2.md)|Required|Required|Yes|  
|[IDebugSymbolSearchEvent2](../vs140/IDebugSymbolSearchEvent2.md)|Allowed, but not required|Allowed, but not required|No|  
|[IDebugThreadCreateEvent2](../vs140/IDebugThreadCreateEvent2.md)|Required|Required|No|  
|[IDebugThreadDestroyEvent2](../vs140/IDebugThreadDestroyEvent2.md)|Required|Required|No|  
|[IDebugThreadNameChangedEvent2](../vs140/IDebugThreadNameChangedEvent2.md)|Allowed, but not required|Allowed, but not required|No|  
  
## See Also  
 [Sending Events](../vs140/Sending-Events.md)