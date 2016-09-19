---
title: "IDebugOutputStringEvent2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 86596fd1-cecc-4813-8add-dc3d70068f9b
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugOutputStringEvent2
This interface is sent by the debug engine (DE) to the session debug manager (SDM) to output a string.  
  
## Syntax  
  
```  
IDebugOutputStringEvent2 : IUnknown  
```  
  
## Notes for Implementers  
 The DE implements this interface to send a string to the **Output** window of the IDE. The [IDebugEvent2](../vs140/IDebugEvent2.md) interface must be implemented on the same object as this interface. The SDM uses [QueryInterface](../vs140/QueryInterface.md) to access the `IDebugEvent2` interface.  
  
## Notes for Callers  
 The DE creates and sends this event object to send a string to the **Output** window. The event is sent by using the [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) callback function that is supplied by the SDM when it is attached to the program being debugged.  
  
## Methods in Vtable Order  
 The following table shows the method of `IDebugOutputStringEvent2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetString](../vs140/IDebugOutputStringEvent2--GetString.md)|Gets the displayable message.|  
  
## Remarks  
 For example, in unmanaged code, the string to be output can originate when the program being debugged sends a string to the Win32 `OutputDebugString` function. This string is intercepted by the DE and sent on to the SDM as the `IDebugOutputStringEvent2` event.  
  
 Use [IDebugMessageEvent2](../vs140/IDebugMessageEvent2.md) to send a message that requires a user response.  
  
 Use [IDebugErrorEvent2](../vs140/IDebugErrorEvent2.md) to send an error message that does not require a response.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [IDebugMessageEvent2](../vs140/IDebugMessageEvent2.md)   
 [IDebugErrorEvent2](../vs140/IDebugErrorEvent2.md)   
 [IDebugEvent2](../vs140/IDebugEvent2.md)   
 [IDebugEventCallback2](../Topic/IDebugEventCallback2.md)