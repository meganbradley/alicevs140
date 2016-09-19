---
title: "IDebugPropertyDestroyEvent2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 301b7a75-ecfa-46f1-9131-66cf3e4be147
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPropertyDestroyEvent2
This interface is sent by the debug engine (DE) to the session debug manager (SDM) when a property that is associated with a specific document is about to be destroyed.  
  
## Syntax  
  
```  
IDebugPropertyDestroyEvent2 : IUnknown  
```  
  
## Notes for Implementers  
 The DE implements this interface to report that a property has been destroyed. The [IDebugEvent2](../vs140/IDebugEvent2.md) interface must be implemented on the same object as this interface. The SDM uses [QueryInterface](../vs140/QueryInterface.md) to access the `IDebugEvent2` interface. This interface is implemented if the DE has previously created a property associated with a script; destroying the property removes the associated script from the IDE.  
  
## Notes for Callers  
 The DE creates and sends this event object to report a property has been destroyed. The event is sent by using the [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) callback function that is supplied by the SDM when it is attached to the program being debugged.  
  
## Methods in Vtable Order  
 The following table shows the method of `IDebugPropertyDestroyEvent2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetDebugProperty](../vs140/IDebugPropertyDestroyEvent2--GetDebugProperty.md)|Gets the property to be destroyed.|  
  
## Remarks  
 See the Remarks for [IDebugPropertyCreateEvent2](../vs140/IDebugPropertyCreateEvent2.md) for details on why these events are used.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugEvent2](../vs140/IDebugEvent2.md)   
 [IDebugEventCallback2](../Topic/IDebugEventCallback2.md)   
 [IDebugProperty2](../vs140/IDebugProperty2.md)   
 [IDebugPropertyCreateEvent2](../vs140/IDebugPropertyCreateEvent2.md)