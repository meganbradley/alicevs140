---
title: "IDebugAddress"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bc709ff7-4966-4f36-9af2-690efe2cea1d
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugAddress
This interface represents the address of an item. It is returned by the symbol handler.  
  
## Syntax  
  
```  
IDebugAddress : IUnknown  
```  
  
## Notes for Implementers  
 A symbol provider implements this interface to represent an address of an object.  
  
## Notes for Callers  
 Many methods on many interfaces return this interface.  
  
## Methods in Vtable Order  
 This interface implements the following method:  
  
|Method|Description|  
|------------|-----------------|  
|[GetAddress](../vs140/IDebugAddress--GetAddress.md)|Retrieves a [DEBUG_ADDRESS](../vs140/DEBUG_ADDRESS.md) structure describing an object and its location.|  
  
## Remarks  
 The symbol provider returns this interface to represent an object and its location within a particular scope (for example, function, method, or class). This interface is returned from and passed to various methods of the symbol provider and expression evaluator. Normally, the symbol provider is the only entity that needs to interpret the contents of this interface.  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Symbol Provider Interfaces](../vs140/Symbol-Provider-Interfaces.md)   
 [DEBUG_ADDRESS](../vs140/DEBUG_ADDRESS.md)