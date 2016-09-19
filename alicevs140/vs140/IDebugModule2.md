---
title: "IDebugModule2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 24c2a126-f4ab-4891-8509-8ef99b994c08
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugModule2
This interface represents a module—that is, an executable unit of a program—such as a DLL.  
  
## Syntax  
  
```  
IDebugModule2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to represent a module and to provide access to information about that module.  
  
## Notes for Callers  
 A call to [IDebugModuleLoadEvent2::GetModule](../vs140/IDebugModuleLoadEvent2--GetModule.md) returns this interface. The DE sends the [IDebugModuleLoadEvent2](../vs140/IDebugModuleLoadEvent2.md) interface to the session debug manager (SDM) using the [IDebugEventCallback2::Event](../vs140/IDebugEventCallback2--Event.md) method.  
  
 This interface can also be returned in a [FRAMEINFO](../vs140/FRAMEINFO.md) structure (which is returned by a call to [IDebugThread2::EnumFrameInfo](../vs140/IDebugThread2--EnumFrameInfo.md)).  
  
 [IEnumDebugModules2::Next](../vs140/IEnumDebugModules2--Next.md) also returns this interface ([IDebugProgram2::EnumModules](../vs140/IDebugProgram2--EnumModules.md) returns the [IEnumDebugModules2](../vs140/IEnumDebugModules2.md) interface).  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugModule2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetInfo](../vs140/IDebugModule2--GetInfo.md)|Gets the [MODULE_INFO](../vs140/MODULE_INFO.md) that describes this module.|  
|[ReloadSymbols_Deprecated](../vs140/IDebugModule2--ReloadSymbols_Deprecated.md)|OBSOLETE. DO NOT USE. Reloads the symbols for this module.|  
  
## Remarks  
 Module information can be displayed in the **Modules** window of the IDE.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [MODULE_INFO](../vs140/MODULE_INFO.md)   
 [IDebugModuleLoadEvent2::GetModule](../vs140/IDebugModuleLoadEvent2--GetModule.md)   
 [FRAMEINFO](../vs140/FRAMEINFO.md)   
 [IEnumDebugModules2](../vs140/IEnumDebugModules2.md)