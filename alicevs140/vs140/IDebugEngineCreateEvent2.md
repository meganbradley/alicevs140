---
title: "IDebugEngineCreateEvent2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 37c0a841-1c8d-4802-a990-36b54bca3ef7
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEngineCreateEvent2
The debug engine (DE) sends this interface to the session debug manager (SDM) when an instance of the DE is created.  
  
## Syntax  
  
```  
IDebugEngineCreateEvent2 : IUnknown  
```  
  
## Notes for Implementers  
 The DE implements this interface as part of its normal operations. The [IDebugEvent2](../vs140/IDebugEvent2.md) interface must be implemented on the same object as this interface (the SDM uses the `QueryInterface` method to access the `IDebugEvent2` interface).  
  
## Notes for Callers  
 The DE creates and sends this event object when the DE has been instantiated. The event is sent by using the [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) callback function that is supplied by the SDM when it attached to the program being debugged.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugEngineCreateEvent2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetEngine](../vs140/IDebugEngineCreateEvent2--GetEngine.md)|Retrieves the object that represents the newly created debug engine (DE).|  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [IDebugEngine2](../vs140/IDebugEngine2.md)   
 [IDebugEvent2](../vs140/IDebugEvent2.md)   
 [IDebugEventCallback2](../Topic/IDebugEventCallback2.md)