---
title: "IEEVisualizerServiceProvider"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 859d1a51-1c65-4c8b-ae74-3b74b181ebcd
caps.latest.revision: 19
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEEVisualizerServiceProvider
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 This interface gives access to a method that can create a visualizer service, which is used to handle type visualizer tasks for the IDE.  
  
## Syntax  
  
```  
IEEVisualizerServiceProvider : IUnknown  
```  
  
## Notes for Implementers  
 Visual Studio implements this interface to create a visualizer service object, which in turn is used to supply class IDs (`CLSID`s) of type visualizers to the Visual Studio IDE.  
  
## Notes for Callers  
 The expression evaluator (EE) calls [IDebugBinder3::GetEEService](../vs140/IDebugBinder3--GetEEService.md) to obtain this interface.  
  
## Methods in Vtable order  
  
|Method|Description|  
|------------|-----------------|  
|[IEEVisualizerServiceProvider::CreateVisualizerService](../vs140/IEEVisualizerServiceProvider--CreateVisualizerService.md)|Creates the visualizer service|  
  
## Remarks  
 The `IEEVisualizerServiceProvider` interface is obtained during the implementation of [IDebugParsedExpression::EvaluateSync](../vs140/IDebugParsedExpression--EvaluateSync.md). The visualizer service that this interface creates is used to supply functionality to an [IDebugProperty3](../vs140/IDebugProperty3.md) interface, which the EE is responsible for implementing. The EE is also responsible for implementing an [IEEVisualizerDataProvider](../vs140/IEEVisualizerDataProvider.md) interface that allows type visualizers to view and modify a property's value.  
  
 See [Visualizing and Viewing Data](../vs140/Visualizing-and-Viewing-Data.md) for details on how these interfaces interact.  
  
## Requirements  
 Header: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Expression Evaluation Interfaces](../vs140/Expression-Evaluation-Interfaces.md)   
 [IDebugParsedExpression::EvaluateSync](../vs140/IDebugParsedExpression--EvaluateSync.md)   
 [IEEVisualizerDataProvider](../vs140/IEEVisualizerDataProvider.md)   
 [IDebugBinder3::GetEEService](../vs140/IDebugBinder3--GetEEService.md)   
 [IDebugProperty3](../vs140/IDebugProperty3.md)   
 [Viewing Data](../vs140/Visualizing-and-Viewing-Data.md)