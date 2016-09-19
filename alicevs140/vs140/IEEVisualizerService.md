---
title: "IEEVisualizerService"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3bdb124b-c582-47ba-b465-13c6a1cdb702
caps.latest.revision: 19
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEEVisualizerService
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 This interface implements key methods that supply functionality to the [IDebugProperty3](../vs140/IDebugProperty3.md) and [IPropertyProxyEESide](../vs140/IPropertyProxyEESide.md) interfaces.  
  
## Syntax  
  
```  
IEEVisualizerService : IUnknown  
```  
  
## Notes for Implementers  
 Visual Studio implements this interface to allow an expression evaluator (EE) to support type visualizers.  
  
## Notes for Callers  
 The EE calls [IEEVisualizerServiceProvider::CreateVisualizerService](../vs140/IEEVisualizerServiceProvider--CreateVisualizerService.md) to obtain this interface as part of its support for type visualizers.  
  
## Methods in Vtable order  
  
|Method|Description|  
|------------|-----------------|  
|[GetCustomViewerCount](../vs140/IEEVisualizerService--GetCustomViewerCount.md)|Retrieves the number of custom viewers about which this service knows.|  
|[GetCustomViewerList](../vs140/IEEVisualizerService--GetCustomViewerList.md)|Retrieves the list of custom viewers.|  
|[GetPropertyProxy](../vs140/IEEVisualizerService--GetPropertyProxy.md)|Returns a proxy object for a property.|  
|[IEEVisualizerService::GetValueDisplayStringCount](../vs140/IEEVisualizerService--GetValueDisplayStringCount.md)|Retrieves the number of value strings to display for the specified property or field.|  
  
## Remarks  
 The IDE uses the [IDebugProperty3](../vs140/IDebugProperty3.md) interface to determine if there are any custom viewers or type visualizers for the property. By creating a visualizer service (with [IEEVisualizerServiceProvider::CreateVisualizerService](../vs140/IEEVisualizerServiceProvider--CreateVisualizerService.md)), the EE can supply the functionality to the `IDebugProperty3` and [IPropertyProxyEESide](../vs140/IPropertyProxyEESide.md) (which supports viewing and changing a property's value) interfaces and thereby support type visualizers.  
  
 If an EE has custom viewers that itself implements, the EE can append the `CLSID`s of those custom viewers to the end of the list returned by [IEEVisualizerService::GetCustomViewerList](../vs140/IEEVisualizerService--GetCustomViewerList.md). This allows an EE to support both type visualizers and its own custom viewers. Just be sure that [IDebugProperty3::GetCustomViewerCount](../vs140/IDebugProperty3--GetCustomViewerCount.md) reflects the addition of any custom viewers.  
  
 See [Type Visualizer and Custom Viewer](../vs140/Type-Visualizer-and-Custom-Viewer.md) for a discussion of the difference between visualizers and viewers.  
  
## Requirements  
 Header: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Expression Evaluation Interfaces](../vs140/Expression-Evaluation-Interfaces.md)   
 [IDebugProperty2](../vs140/IDebugProperty2.md)   
 [IDebugProperty3](../vs140/IDebugProperty3.md)   
 [IPropertyProxyEESide](../vs140/IPropertyProxyEESide.md)   
 [IEEVisualizerServiceProvider::CreateVisualizerService](../vs140/IEEVisualizerServiceProvider--CreateVisualizerService.md)   
 [Type Visualizer and Custom Viewer](../vs140/Type-Visualizer-and-Custom-Viewer.md)