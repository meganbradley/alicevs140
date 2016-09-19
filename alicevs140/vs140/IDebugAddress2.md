---
title: "IDebugAddress2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b150e0ed-4ac0-4f8c-9732-4b3e54b9d243
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugAddress2
This interface provides access to the ID of the process that owns the object whose address is represented by this interface.  
  
## Syntax  
  
```  
IDebugAddress2 : IDebugAddress  
```  
  
## Notes for Implementers  
 A symbol provider implements this interface on the same object that implements the [IDebugAddress](../vs140/IDebugAddress.md) interface. This interface provides access to the ID of the process that owns the object that is related to this address.  
  
## Notes for Callers  
 Use [QueryInterface](../vs140/QueryInterface.md) to obtain this interface from the [IDebugAddress](../vs140/IDebugAddress.md) interface.  
  
## Methods in vtable Order  
 In addition to the methods inherited from the [IDebugAddress](../vs140/IDebugAddress.md) interface, this interface implements the following method:  
  
|Method|Description|  
|------------|-----------------|  
|[GetProcessID](../vs140/IDebugAddress2--GetProcessID.md)|Retrieves the ID of the process that owns the object represented by this interface.|  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Symbol Provider Interfaces](../vs140/Symbol-Provider-Interfaces.md)   
 [IDebugAddress](../vs140/IDebugAddress.md)