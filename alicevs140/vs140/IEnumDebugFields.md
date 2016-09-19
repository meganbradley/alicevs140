---
title: "IEnumDebugFields"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 403c2a51-3ba5-431f-a1dd-2f3b2046c00c
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugFields
This interface represents a collection of objects implementing the [IDebugField](../vs140/IDebugField.md) interface.  
  
## Syntax  
  
```  
IEnumDebugFields : IUnknown  
```  
  
## Notes for Implementers  
 This interface is implemented by the symbol provider to provide sets of objects that implement the [IDebugField](../vs140/IDebugField.md) interface. Note that this is not a standard COM enumeration due to the presence of the [IEnumDebugFields::GetCount](../vs140/IEnumDebugFields--GetCount.md) method.  
  
## Notes for Callers  
 This interface is returned by [IDebugSymbolProvider::GetMethodFieldsByName](../vs140/IDebugSymbolProvider--GetMethodFieldsByName.md) and [IDebugSymbolProvider::GetNamespacesUsedAtAddress](../vs140/IDebugSymbolProvider--GetNamespacesUsedAtAddress.md).  
  
## Methods in Vtable order  
 This interface implements the following methods.  
  
|Method|Description|  
|------------|-----------------|  
|[IEnumDebugFields::Next](../vs140/IEnumDebugFields--Next.md)|Retrieves the next set of [IDebugField](../vs140/IDebugField.md) objects from the enumeration.|  
|[IEnumDebugFields::Skip](../vs140/IEnumDebugFields--Skip.md)|Skips a specified number of entries.|  
|[IEnumDebugFields::Reset](../vs140/IEnumDebugFields--Reset.md)|Resets the enumeration to the first entry.|  
|[IEnumDebugFields::Clone](../vs140/IEnumDebugFields--Clone.md)|Retrieves a copy of the current enumeration.|  
|[IEnumDebugFields::GetCount](../vs140/IEnumDebugFields--GetCount.md)|Retrieves the number of entries in the enumeration.|  
  
## Remarks  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Symbol Provider Interfaces](../vs140/Symbol-Provider-Interfaces.md)   
 [IDebugField](../vs140/IDebugField.md)   
 [IDebugSymbolProvider::GetMethodFieldsByName](../vs140/IDebugSymbolProvider--GetMethodFieldsByName.md)   
 [IDebugSymbolProvider::GetNamespacesUsedAtAddress](../vs140/IDebugSymbolProvider--GetNamespacesUsedAtAddress.md)