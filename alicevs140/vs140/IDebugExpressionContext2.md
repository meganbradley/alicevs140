---
title: "IDebugExpressionContext2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 577fdaae-4b2d-4112-9839-ab899535fa6f
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugExpressionContext2
This interface represents a context for expression evaluation  
  
## Syntax  
  
```  
IDebugExpressionContext2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to represent a context in which an expression can be evaluated.  
  
## Notes for Callers  
 A call to [IDebugStackFrame2::GetExpressionContext](../vs140/IDebugStackFrame2--GetExpressionContext.md) returns the this interface. This interface is accessible only when the program being debugged has been paused and a stack frame is available.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugExpressionContext2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetName](../vs140/IDebugExpressionContext2--GetName.md)|Retrieves the name of the evaluation context.|  
|[ParseText](../vs140/IDebugExpressionContext2--ParseText.md)|Parses a text-based expression for evaluation.|  
  
## Remarks  
 An evaluation context can be thought of as a scope for performing expression evaluation.  
  
 When a program has halted, the session debug manager (SDM) obtains a stack frame from the DE with a call to [IDebugThread2::EnumFrameInfo](../vs140/IDebugThread2--EnumFrameInfo.md). The SDM then calls [IDebugStackFrame2::GetExpressionContext](../vs140/IDebugStackFrame2--GetExpressionContext.md) to get the `IDebugExpressionContext2` interface. This is followed by a call to [IDebugExpressionContext2::ParseText](../vs140/IDebugExpressionContext2--ParseText.md) to create an [IDebugExpression2](../vs140/IDebugExpression2.md) interface, which represents the parsed expression ready to be evaluated.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [GetExpressionContext](../vs140/IDebugStackFrame2--GetExpressionContext.md)   
 [IDebugExpression2](../vs140/IDebugExpression2.md)