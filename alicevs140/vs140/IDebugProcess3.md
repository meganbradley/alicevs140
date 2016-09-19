---
title: "IDebugProcess3"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7bd6b952-cf34-4e66-b8f6-d472dac3748f
caps.latest.revision: 26
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess3
This interface represents a running process and its programs. This interface exists as a replacement to several methods in the [IDebugProgram2](../vs140/IDebugProgram2.md) interface. It provides control over all programs in the process.  
  
> [!NOTE]
>  [IDebugProgram2::Continue](../vs140/IDebugProgram2--Continue.md), [IDebugProgram2::Execute](../vs140/IDebugProgram2--Execute.md), and [IDebugProgram2::Step](../vs140/IDebugProgram2--Step.md) methods are deprecated and should no longer be used. Use the corresponding methods on the `IDebugProcess3` interface instead.  
  
## Syntax  
  
```  
IDebugProcess3 : IDebugProcess2  
```  
  
## Notes for Implementers  
 This interface is implemented by a custom port supplier to manage programs as a group. When programs are managed as a group, you can control their execution and establish a language for an expression evaluator. This interface must be implemented by the port supplier.  
  
## Notes for Callers  
 This interface is called primarily by the session debug manager (SDM) in order to interact with a group of programs identified in this process.  
  
 Call [QueryInterface](../vs140/QueryInterface.md) on an [IDebugProcess2](../vs140/IDebugProcess2.md) interface to obtain this interface.  
  
## Methods in Vtable Order  
 In addition to the methods inherited from [IDebugProcess2](../vs140/IDebugProcess2.md), `IDebugProcess3` implements the following methods.  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugProcess3::Continue](../vs140/IDebugProcess3--Continue.md)|Continues execution of or stepping through a process.|  
|[IDebugProcess3::Execute](../vs140/IDebugProcess3--Execute.md)|Begins execution of a process.|  
|[IDebugProcess3::Step](../vs140/IDebugProcess3--Step.md)|Steps forward one instruction or statement in the process.|  
|[IDebugProcess3::GetDebugReason](../vs140/IDebugProcess3--GetDebugReason.md)|Gets the reason that the process was launched for debugging.|  
|[IDebugProcess3::SetHostingProcessLanguage](../vs140/IDebugProcess3--SetHostingProcessLanguage.md)|Sets the hosting language so that the debug engine can load the appropriate expression evaluator.|  
|[IDebugProcess3::GetHostingProcessLanguage](../vs140/IDebugProcess3--GetHostingProcessLanguage.md)|Retrieves the language currently set for this process.|  
|[IDebugProcess3::DisableENC](../vs140/IDebugProcess3--DisableENC.md)|Disables Edit and Continue (ENC) for this process.<br /><br /> A custom port supplier does not implement this method (it should always return `E_NOTIMPL`).|  
|[IDebugProcess3::GetENCAvailableState](../vs140/IDebugProcess3--GetENCAvailableState.md)|Get the ENC state for this process.<br /><br /> A custom port supplier does not implement this method (it should always return `E_NOTIMPL`).|  
|[IDebugProcess3::GetEngineFilter](../vs140/IDebugProcess3--GetEngineFilter.md)|Retrieves an array of unique identifiers for available debug engines.|  
  
## Requirements  
 Header: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugProcess2](../vs140/IDebugProcess2.md)   
 [IDebugProgram2](../vs140/IDebugProgram2.md)