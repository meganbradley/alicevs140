---
title: "IDebugBinder3"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 92353a74-dc74-4f93-8762-61d6b220478c
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBinder3
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 This interface provides access to types, aliases, and custom visualizer services.  
  
## Syntax  
  
```  
IDebugBinder3 : IDebugBinder  
```  
  
## Notes for Implementers  
 A debug engine implements this interface to support aliases, custom visualizer services, and access to object type information.  
  
## Notes for Callers  
 An [IDebugBinder](../vs140/IDebugBinder.md) interface obtains this interface by using [QueryInterface](../vs140/QueryInterface.md).  
  
## Methods in Vtable order  
 In addition to the methods provided by the [IDebugBinder](../vs140/IDebugBinder.md) interface, this interface implements the following:  
  
|Method|Description|  
|------------|-----------------|  
|[GetMemoryObject](../vs140/IDebugBinder3--GetMemoryObject.md)|Retrieves a memory object representing the memory to which this object is bound.|  
|[GetExceptionObjectAndType](../vs140/IDebugBinder3--GetExceptionObjectAndType.md)|Retrieves the exception associated with this object (if any),|  
|[FindAlias](../vs140/IDebugBinder3--FindAlias.md)|Retrieves an alias given its name,|  
|[GetAllAliases](../vs140/IDebugBinder3--GetAllAliases.md)|Retrieves an array of all aliases for this object,|  
|[GetTypeArgumentCount](../vs140/IDebugBinder3--GetTypeArgumentCount.md)|Gets the number of argument types associated with this object,|  
|[GetTypeArguments](../vs140/IDebugBinder3--GetTypeArguments.md)|Retrieves a list of argument types associated with this object,|  
|[GetEEService](../vs140/IDebugBinder3--GetEEService.md)|Gets an interface to a visualizer service,|  
|[IDebugBinder3::GetMemoryContext64](../vs140/IDebugBinder3--GetMemoryContext64.md)|Converts either an object location or a 64-bit memory address to a memory context.|  
  
## Requirements  
 Header: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Expression Evaluation Interfaces](../vs140/Expression-Evaluation-Interfaces.md)   
 [IDebugBinder](../vs140/IDebugBinder.md)