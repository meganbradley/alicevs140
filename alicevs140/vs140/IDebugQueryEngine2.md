---
title: "IDebugQueryEngine2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8f0e1838-a818-4459-9138-a3dceb7408de
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugQueryEngine2
This interface lets the session debug manager (SDM) retrieve an interface that represents the debug engine (DE).  
  
## Syntax  
  
```  
IDebugQueryEngine2 : IUnknown  
```  
  
## Notes for Implementers  
 The DE implements this interface on the objects that implement the most common DE interfaces (such as [IDebugProgram2](../vs140/IDebugProgram2.md), [IDebugThread2](../vs140/IDebugThread2.md), and [IDebugStackFrame2](../vs140/IDebugStackFrame2.md)) in order to allow access to the [IDebugEngine2](../vs140/IDebugEngine2.md) interface of the DE itself.  
  
## Notes for Callers  
 Call [QueryInterface](../vs140/QueryInterface.md) on a typical DE interface to obtain this interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugQueryEngine2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetEngineInterface](../vs140/IDebugQueryEngine2--GetEngineInterface.md)|Gets a custom debug engine (DE) interface.|  
  
## Remarks  
 This interface is typically implemented in the object that implements the [IDebugProgram2](../vs140/IDebugProgram2.md) interface in order to support causality-ordered stepping through functions; that is, when the debugger is stepping out of a function, the next function to execute may not be the previous function on the stack but a function in another thread altogether. For a definition of "causality," see the [Visual Studio Debugging Glossary](../vs140/Visual-Studio-Debugger-Glossary.md).  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugProgram2](../vs140/IDebugProgram2.md)   
 [IDebugThread2](../vs140/IDebugThread2.md)   
 [IDebugStackFrame2](../vs140/IDebugStackFrame2.md)   
 [IDebugEngine2](../vs140/IDebugEngine2.md)