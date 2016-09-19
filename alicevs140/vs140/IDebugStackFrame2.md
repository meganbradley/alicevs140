---
title: "IDebugStackFrame2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bd212a6a-dcc6-4756-a77a-e8dfda38b104
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugStackFrame2
This interface represents a single stack frame in a call stack in a particular thread.  
  
## Syntax  
  
```  
IDebugStackFrame2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to represent a stack frame.  
  
## Notes for Callers  
 Call [IDebugThread2::EnumFrameInfo](../vs140/IDebugThread2--EnumFrameInfo.md) to retrieve an [IEnumDebugFrameInfo2](../vs140/IEnumDebugFrameInfo2.md) interface. Call [IEnumDebugFrameInfo2::Next](../vs140/IEnumDebugFrameInfo2--Next.md) to retrieve a [FRAMEINFO](../vs140/FRAMEINFO.md) structure that contains the `IDebugStackFrame2` interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugStackFrame2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetCodeContext](../vs140/IDebugStackFrame2--GetCodeContext.md)|Gets the code context for this stack frame.|  
|[GetDocumentContext](../vs140/IDebugStackFrame2--GetDocumentContext.md)|Gets the document context for this stack frame.|  
|[GetName](../vs140/IDebugStackFrame2--GetName.md)|Gets the name of the stack frame.|  
|[GetInfo](../vs140/IDebugStackFrame2--GetInfo.md)|Gets a description of the stack frame.|  
|[GetPhysicalStackRange](../vs140/IDebugStackFrame2--GetPhysicalStackRange.md)|Gets a machine-dependent representation of the range of physical addresses associated with a stack frame.|  
|[GetExpressionContext](../vs140/IDebugStackFrame2--GetExpressionContext.md)|Gets an evaluation context for doing expression evaluation within the current context of a stack frame and thread.|  
|[GetLanguageInfo](../vs140/IDebugStackFrame2--GetLanguageInfo.md)|Gets the language associated with a stack frame.|  
|[GetDebugProperty](../vs140/IDebugStackFrame2--GetDebugProperty.md)|Gets a description of the properties associated with a stack frame.|  
|[EnumProperties](../vs140/IDebugStackFrame2--EnumProperties.md)|Creates an enumerator for stack frame properties.|  
|[GetThread](../vs140/IDebugStackFrame2--GetThread.md)|Gets the thread associated with a stack frame.|  
  
## Remarks  
 This interface is obtained only when the program being debugged has been stopped at a breakpoint (either caused by a user-set breakpoint or an exception). From this interface, an expression context can be obtained to evaluate expressions, a list of registers can be returned, or the call stack can be obtained and examined.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)