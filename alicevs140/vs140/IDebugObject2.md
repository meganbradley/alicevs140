---
title: "IDebugObject2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ef640967-8adb-4793-994d-ae1736510891
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugObject2
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 This interface provides additional information about an object.  
  
## Syntax  
  
```  
IDebugObject2 : IDebugObject  
```  
  
## Notes for Implementers  
 The expression evaluator implements this interface to offer support for aliases and access to information about the object.  
  
## Notes for Callers  
 An [IDebugObject](../vs140/IDebugObject.md) interface can obtain this interface by using [QueryInterface](../vs140/QueryInterface.md). Also, [IDebugAlias::GetObject](../vs140/IDebugAlias--GetObject.md) returns this interface.  
  
## Methods in Vtable order  
 In addition to the methods on the [IDebugObject](../vs140/IDebugObject.md) interface, the `IDebugObject2` interface implements the following:  
  
|Method|Description|  
|------------|-----------------|  
|[GetBackingFieldForProperty](../vs140/IDebugObject2--GetBackingFieldForProperty.md)|Gets the field or variable (if any) that may be backing the property represented by this object.|  
|[GetICorDebugValue](../vs140/IDebugObject2--GetICorDebugValue.md)|Gets the managed code object representing the value of this object.|  
|[CreateAlias](../vs140/IDebugObject2--CreateAlias.md)|Creates a unique ID for this object or returns an existing alias.|  
|[GetAlias](../vs140/IDebugObject2--GetAlias.md)|Gets the alias associated with this object, if any.|  
|[GetField](../vs140/IDebugObject2--GetField.md)|Gets the type of this object.|  
|[IsUserData](../vs140/IDebugObject2--IsUserData.md)|Determines whether this object represents user data.|  
|[IsEncOutdated](../vs140/IDebugObject2--IsEncOutdated.md)|Determines whether the Edit and Continue state is no longer valid.<br /><br /> A custom expression evaluator does not implement this method (it should always return `E_NOTIMPL`).|  
  
## Remarks  
 See [IDebugAlias](../vs140/IDebugAlias.md) for a discussion on aliases.  
  
## Requirements  
 Header: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Expression Evaluation Interfaces](../vs140/Expression-Evaluation-Interfaces.md)   
 [IDebugObject](../vs140/IDebugObject.md)   
 [IDebugAlias](../vs140/IDebugAlias.md)   
 [IDebugAlias::GetObject](../vs140/IDebugAlias--GetObject.md)