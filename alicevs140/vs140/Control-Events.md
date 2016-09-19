---
title: "Control Events"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0fc63484-5fb6-4887-9ea4-1905b459ca9d
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Control Events
You must send events during the controlled execution of your program. All of the events are sent using the [IDebugEvent2](../vs140/IDebugEvent2.md) interface and have attributes that require you to implement the [IDebugEvent2::GetAttributes](../vs140/IDebugEvent2--GetAttributes.md) method.  
  
## Additional Methods  
 Some events require implementation of additional methods, as follows:  
  
-   Sending the [IDebugEngineCreateEvent2](../vs140/IDebugEngineCreateEvent2.md) interface when the debug engine (DE) is initialized requires you to implement the [IDebugEngineCreateEvent2::GetEngine](../vs140/IDebugEngineCreateEvent2--GetEngine.md) method.  
  
-   Execution control requires implementation of such control events as the [IDebugBreakEvent2](../vs140/IDebugBreakEvent2.md) and[IDebugStepCompleteEvent2](../vs140/IDebugStepCompleteEvent2.md) interfaces. **IDebugBreakEvent2** is required only for asynchronous breaks.  
  
-   Stepping into functions requires implementation of the [IDebugStepCompleteEvent2](../vs140/IDebugStepCompleteEvent2.md) interface and its methods.  
  
 Events deriving from breakpoints require implementation of the [IDebugBreakpointErrorEvent2](../vs140/IDebugBreakpointErrorEvent2.md), [IDebugBreakpointEvent2](../vs140/IDebugBreakpointEvent2.md), and [IDebugBreakpointBoundEvent2](../vs140/IDebugBreakpointBoundEvent2.md) interfaces, as well as the [IDebugBreakpointBoundEvent2::GetPendingBreakpoint](../vs140/IDebugBreakpointBoundEvent2--GetPendingBreakpoint.md) and [EnumBoundBreakpoints](../vs140/IDebugBreakpointBoundEvent2--EnumBoundBreakpoints.md) methods.  
  
 Asynchronous expression evaluation requires you to implement the [IDebugExpressionEvaluationCompleteEvent2](../vs140/IDebugExpressionEvaluationCompleteEvent2.md) interface and its [IDebugExpressionEvaluationCompleteEvent2::GetExpression](../vs140/IDebugExpressionEvaluationCompleteEvent2--GetExpression.md)[and GetResult](../vs140/IDebugExpressionEvaluationCompleteEvent2--GetResult.md) methods.  
  
 Synchronous events require implementing the [IDebugEngine2::ContinueFromSynchronousEvent](../vs140/IDebugEngine2--ContinueFromSynchronousEvent.md) method.  
  
 For your engine to write string-style output, you must implement the [IDebugOutputStringEvent2::GetString](../vs140/IDebugOutputStringEvent2--GetString.md) method.  
  
## See Also  
 [Execution Control and State Evaluation](../vs140/Execution-Control-and-State-Evaluation.md)