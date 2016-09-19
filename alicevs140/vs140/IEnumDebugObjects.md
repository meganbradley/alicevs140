---
title: "IEnumDebugObjects"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0950364c-6c8a-4b6c-ba37-c6aa359fa72c
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugObjects
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 This interface represents a collection of objects implementing the [IDebugObject](../vs140/IDebugObject.md) interface.  
  
## Syntax  
  
```  
IEnumDebugObjects : IUnknown  
```  
  
## Notes for Implementers  
 The expression evaluator implements this interface to provide sets of objects that implement the [IDebugObject](../vs140/IDebugObject.md) interface. Note that this is not a standard COM enumeration due to the presence of the [IEnumDebugObjects::GetCount](../vs140/IEnumDebugObjects--GetCount.md) method.  
  
## Notes for Callers  
 [IDebugArrayObject::GetElements](../vs140/IDebugArrayObject--GetElements.md) returns this interface.  
  
## Methods in Vtable order  
 This interface implements the following methods.  
  
|Method|Description|  
|------------|-----------------|  
|[IEnumDebugObjects::Next](../vs140/IEnumDebugObjects--Next.md)|Retrieves the next set of [IDebugObject](../vs140/IDebugObject.md) objects from the enumeration.|  
|[IEnumDebugObjects::Skip](../vs140/IEnumDebugObjects--Skip.md)|Skips a specified number of entries.|  
|[IEnumDebugObjects::Reset](../vs140/IEnumDebugObjects--Reset.md)|Resets the enumeration to the first entry.|  
|[IEnumDebugObjects::Clone](../vs140/IEnumDebugObjects--Clone.md)|Retrieves a copy of the current enumeration.|  
|[IEnumDebugObjects::GetCount](../vs140/IEnumDebugObjects--GetCount.md)|Retrieves the number of entries in the enumeration.|  
  
## Remarks  
 This interface allows a debug engine to enumerate over a set of objects in an array.  
  
## Requirements  
 Header: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [IDebugObject](../vs140/IDebugObject.md)   
 [IDebugArrayObject::GetElements](../vs140/IDebugArrayObject--GetElements.md)