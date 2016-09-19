---
title: "IDebugReturnValueEvent2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2daded43-e427-4fbb-a19e-f3834e3723af
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugReturnValueEvent2
This interface is sent by the debug engine (DE) to the session debug manager (SDM) after stepping out of or over a function.  
  
## Syntax  
  
```  
IDebugReturnValueEvent2 : IUnknown  
```  
  
## Notes for Implementers  
 The DE implements this interface to report the return value from a function that has been stepped out of or over. The [IDebugEvent2](../vs140/IDebugEvent2.md) interface must be implemented on the same object as this interface. The SDM uses [QueryInterface](../vs140/QueryInterface.md) to access the `IDebugEvent2` interface.  
  
## Notes for Callers  
 The DE creates and sends this event object to report the return value of a function. The event is sent by using the [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) callback function that is supplied by the SDM when it is attached to the program being debugged.  
  
## Methods in Vtable Order  
 The following table shows the method of `IDebugReturnValueEvent2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetReturnValue](../vs140/IDebugReturnValueEvent2--GetReturnValue.md)|Gets the value returned on stepping out of a function.|  
  
## Remarks  
 The value returned by a function can be obtained by calling [IDebugReturnValueEvent2::GetReturnValue](../vs140/IDebugReturnValueEvent2--GetReturnValue.md). The value returned appears in the **Autos** window.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugEvent2](../vs140/IDebugEvent2.md)