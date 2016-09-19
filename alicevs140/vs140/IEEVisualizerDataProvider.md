---
title: "IEEVisualizerDataProvider"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5fdfe6e3-b94e-4edb-acc5-41d8773d8ca5
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEEVisualizerDataProvider
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 This interface provides the ability to change an object's value through a type visualizer.  
  
## Syntax  
  
```  
IEEVisualizerDataProvider : IUnknown  
```  
  
## Notes for Implementers  
 The expression evaluator implements this interface to support modifying data on a property object through a type visualizer.  
  
## Notes for Callers  
 This interface is used in creating the [IEEVisualizerService](../vs140/IEEVisualizerService.md) object through a call to [IEEVisualizerServiceProvider::CreateVisualizerService](../vs140/IEEVisualizerServiceProvider--CreateVisualizerService.md). See [Visualizing and Viewing Data](../vs140/Visualizing-and-Viewing-Data.md) for more details.  
  
## Methods in Vtable order  
  
|Method|Description|  
|------------|-----------------|  
|[CanSetObjectForVisualizer](../vs140/IEEVisualizerDataProvider--CanSetObjectForVisualizer.md)|Determines if it is possible to update the object (and subsequently, its value) that this visualizer is representing.|  
|[GetNewObjectForVisualizer](../vs140/IEEVisualizerDataProvider--GetNewObjectForVisualizer.md)|Forces a re-evaluation of the object for this visualizer.|  
|[GetObjectForVisualizer](../vs140/IEEVisualizerDataProvider--GetObjectForVisualizer.md)|Gets an existing object for this visualizer (no evaluation is done).|  
|[SetObjectForVisualizer](../vs140/IEEVisualizerDataProvider--SetObjectForVisualizer.md)|Updates the object for this visualizer, thereby changing the value the visualizer presents.|  
  
## Remarks  
 The visualizer service (as represented by the [IEEVisualizerService](../vs140/IEEVisualizerService.md) interface and returned by [IEEVisualizerServiceProvider::CreateVisualizerService](../vs140/IEEVisualizerServiceProvider--CreateVisualizerService.md)) keeps a reference to the object implementing the `IEEVisualizerDataProvider` interface. As a result, the `IEEVisualizerDataProvider` interface should not be implemented on the same object that implements the [IDebugProperty2](../vs140/IDebugProperty2.md) if that object maintains a reference to the `IEEVisualizerService` object: a circular reference results and a deadlock occurs when the objects are destroyed. The recommended approach is to implement `IEEVisualizerDataProvider` on a separate object to which the `IDebugProperty2` object delegates without calling `IUnknown::AddRef` on it.  
  
## Requirements  
 Header: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Expression Evaluation Interfaces](../vs140/Expression-Evaluation-Interfaces.md)   
 [IDebugProperty2](../vs140/IDebugProperty2.md)   
 [IEEVisualizerService](../vs140/IEEVisualizerService.md)   
 [IEEVisualizerServiceProvider](../vs140/IEEVisualizerServiceProvider.md)   
 [Visualizing Data (Visual Studio Debugging SDK)](../vs140/Visualizing-and-Viewing-Data.md)