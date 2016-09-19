---
title: "IDebugExpression2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f5e4b124-1e30-47c8-a511-80084a02dba5
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugExpression2
This interface represents a parsed expression ready for binding and evaluating.  
  
## Syntax  
  
```  
IDebugExpression2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to represent a parsed expression ready to be evaluated.  
  
## Notes for Callers  
 A call to [IDebugExpressionContext2::ParseText](../vs140/IDebugExpressionContext2--ParseText.md) returns this interface. [IDebugStackFrame2::GetExpressionContext](../vs140/IDebugStackFrame2--GetExpressionContext.md) returns the [IDebugExpressionContext2](../vs140/IDebugExpressionContext2.md) interface. These interfaces are accessible only when the program being debugged has been paused and a stack frame is available.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugExpression2`.  
  
|Method|Description|  
|------------|-----------------|  
|[EvaluateAsync](../vs140/IDebugExpression2--EvaluateAsync.md)|Evaluates this expression asynchronously.|  
|[Abort](../vs140/IDebugExpression2--Abort.md)|Ends asynchronous expression evaluation.|  
|[EvaluateSync](../vs140/IDebugExpression2--EvaluateSync.md)|Evaluates this expression synchronously.|  
  
## Remarks  
 When a program has halted, the session debug manager (SDM) obtains a stack frame from the DE with a call to [IDebugThread2::EnumFrameInfo](../vs140/IDebugThread2--EnumFrameInfo.md). The SDM then calls [IDebugStackFrame2::GetExpressionContext](../vs140/IDebugStackFrame2--GetExpressionContext.md) to get the [IDebugExpressionContext2](../vs140/IDebugExpressionContext2.md) interface. This is followed by a call to [IDebugExpressionContext2::ParseText](../vs140/IDebugExpressionContext2--ParseText.md) to create the `IDebugExpression2` interface, which represents the parsed expression ready to be evaluated.  
  
 The SDM calls either [IDebugExpression2::EvaluateSync](../vs140/IDebugExpression2--EvaluateSync.md) or [IDebugExpression2::EvaluateAsync](../vs140/IDebugExpression2--EvaluateAsync.md) to actually evaluate the expression and produce a value.  
  
 In an implementation of `IDebugExpressionContext2::ParseText`, the DE uses COM's `CoCreateInstance` function to instantiate an expression evaluator and get an [IDebugExpressionEvaluator](../vs140/IDebugExpressionEvaluator.md) interface (see the Example in the `IDebugExpressionEvaluator` interface). The DE then calls [IDebugExpressionEvaluator::Parse](../vs140/IDebugExpressionEvaluator--Parse.md) to obtain an [IDebugParsedExpression](../vs140/IDebugParsedExpression.md) interface. This interface is used in the implementation of `IDebugExpression2::EvaluateSync` and `IDebugExpression2::EvaluateAsync` to perform the evaluation.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [GetExpression](../vs140/IDebugExpressionEvaluationCompleteEvent2--GetExpression.md)