---
title: "IEnumDebugAddresses"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5f6f6751-e6d8-4c5a-8e81-414b6e5d8cc5
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugAddresses
This interface represents a collection of objects implementing the [IDebugAddress](../vs140/IDebugAddress.md) interface.  
  
## Syntax  
  
```  
IEnumDebugAdresses : IUnknown  
```  
  
## Notes for Implementers  
 This interface is implemented by the symbol provider to provide sets of objects that implement the [IDebugAddress](../vs140/IDebugAddress.md) interface. Note that this is not a standard COM enumeration due to the presence of the [IEnumDebugAddresses::GetCount](../vs140/IEnumDebugAddresses--GetCount.md) method.  
  
## Notes for Callers  
 This interface is returned by [IDebugSymbolProvider::GetAddressesFromContext](../vs140/IDebugSymbolProvider--GetAddressesFromContext.md) and [IDebugSymbolProvider::GetAddressesFromPosition](../vs140/IDebugSymbolProvider--GetAddressesFromPosition.md).  
  
## Methods in Vtable order  
 This interface implements the following methods.  
  
|Method|Description|  
|------------|-----------------|  
|[IEnumDebugAddresses::Next](../vs140/IEnumDebugAddresses--Next.md)|Retrieves the next set of [IDebugAddress](../vs140/IDebugAddress.md) objects from the enumeration.|  
|[IEnumDebugAddresses::Skip](../vs140/IEnumDebugAddresses--Skip.md)|Skips a specified number of entries.|  
|[IEnumDebugAddresses::Reset](../vs140/IEnumDebugAddresses--Reset.md)|Resets the enumeration to the first entry.|  
|[IEnumDebugAddresses::Clone](../vs140/IEnumDebugAddresses--Clone.md)|Retrieves a copy of the current enumeration.|  
|[IEnumDebugAddresses::GetCount](../vs140/IEnumDebugAddresses--GetCount.md)|Retrieves the number of entries in the enumeration.|  
  
## Remarks  
 This interface is typically used by the debug engine to help determine the appropriate address to give to the expression evaluator.  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Symbol Provider Interfaces](../vs140/Symbol-Provider-Interfaces.md)   
 [IDebugAddress](../vs140/IDebugAddress.md)   
 [IDebugSymbolProvider::GetAddressesFromContext](../vs140/IDebugSymbolProvider--GetAddressesFromContext.md)   
 [IDebugSymbolProvider::GetAddressesFromPosition](../vs140/IDebugSymbolProvider--GetAddressesFromPosition.md)