---
title: "IDebugAlias"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3cc4c9a4-7805-4239-b00e-eb4a024f3c55
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugAlias
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Represents a numeric alias for a variable. An alias is simply a different name for a variable.  
  
## Syntax  
  
```  
IDebugAlias : IUnknown  
```  
  
## Notes for Implementers  
 The expression evaluator (EE) implements this interface to support numerical aliases for variables.  
  
## Notes for Callers  
 [IDebugObject2::CreateAlias](../vs140/IDebugObject2--CreateAlias.md) creates an alias for a particular object. To search for aliases, use [IDebugBinder3::FindAlias](../vs140/IDebugBinder3--FindAlias.md) or [IDebugBinder3::GetAllAliases](../vs140/IDebugBinder3--GetAllAliases.md).  
  
## Methods in Vtable Order  
 The following methods are defined in the `IDebugAlias` interface.  
  
|Method|Description|  
|------------|-----------------|  
|[GetObject](../vs140/IDebugAlias--GetObject.md)|Gets the object to which this alias refers.|  
|[GetName](../vs140/IDebugAlias--GetName.md)|Gets the alias name.|  
|[GetICorDebugValue](../vs140/IDebugAlias--GetICorDebugValue.md)|Retrieves an `ICorDebugValue` interface that provides access to managed code information about this object (managed code only).|  
|[Dispose](../vs140/IDebugAlias--Dispose.md)|Marks this alias as no longer being used.|  
  
## Remarks  
 An alias is a decimal number in string form followed by the # character, for example, 1001#.  
  
## Requirements  
 Header: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Expression Evaluation Interfaces](../vs140/Expression-Evaluation-Interfaces.md)   
 [IDebugObject2::CreateAlias](../vs140/IDebugObject2--CreateAlias.md)   
 [IDebugBinder3::FindAlias](../vs140/IDebugBinder3--FindAlias.md)   
 [IDebugBinder3::GetAllAliases](../vs140/IDebugBinder3--GetAllAliases.md)