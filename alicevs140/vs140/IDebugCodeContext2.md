---
title: "IDebugCodeContext2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3670439e-2171-405d-9d77-dedb0f1cba93
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCodeContext2
This interface represents the starting position of a code instruction. For most run-time architectures today, a code context can be thought of as an address in a program's execution stream.  
  
## Syntax  
  
```  
IDebugCodeContext2 : IDebugMemoryContext2  
```  
  
## Notes for Implementers  
 The debug engine implements this interface to relate the position of a code instruction to a document position.  
  
## Notes for Callers  
 Methods on many interfaces return this interface, most typically, [IDebugStackFrame2::GetCodeContext](../vs140/IDebugStackFrame2--GetCodeContext.md). It is also used extensively with the [IDebugDisassemblyStream2](../vs140/IDebugDisassemblyStream2.md) interface as well as in breakpoint resolution information.  
  
## Methods in Vtable Order  
 In addition to the methods on the [IDebugMemoryContext2](../vs140/IDebugMemoryContext2.md) interface, this interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[GetDocumentContext](../vs140/IDebugCodeContext2--GetDocumentContext.md)|Gets the document context that corresponds to the active code context.|  
|[GetLanguageInfo](../vs140/IDebugCodeContext2--GetLanguageInfo.md)|Gets the language information for this code context.|  
  
## Remarks  
 The key difference between an `IDebugCodeContext2` interface and an [IDebugMemoryContext2](../vs140/IDebugMemoryContext2.md) interface is that an `IDebugCodeContext2` is always instruction-aligned. This means that an `IDebugCodeContext2` is always pointing to the beginning of an instruction, whereas an `IDebugMemoryContext2` may point to any byte of memory in the run-time architecture. `IDebugCodeContext2` is incremented by instructions rather than by the basic storage size (typically byte).  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [GetDisassemblyStream](../vs140/IDebugProgram2--GetDisassemblyStream.md)   
 [CanSetNextStatement](../vs140/IDebugThread2--CanSetNextStatement.md)   
 [SetNextStatement](../vs140/IDebugThread2--SetNextStatement.md)   
 [GetCodeContext](../vs140/IDebugCanStopEvent2--GetCodeContext.md)   
 [GetCodeContext](../vs140/IDebugStackFrame2--GetCodeContext.md)   
 [Next](../vs140/IEnumDebugCodeContexts2--Next.md)   
 [IDebugMemoryContext2](../vs140/IDebugMemoryContext2.md)