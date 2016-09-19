---
title: "IPropertyProxyProvider"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 52e9f7fc-6fe0-4d23-890b-5673dca8c3cb
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IPropertyProxyProvider
This interface supplies a proxy interface to view and change an object's data.  
  
## Syntax  
  
```  
IPropertyProxyProvider : IUnknown  
```  
  
## Notes for Implementers  
 The expression evaluator (EE) implements this interface on the same object that implements the [IDebugProperty3](../vs140/IDebugProperty3.md) interface as part of the EE's support of type visualizers.  
  
## Notes for Callers  
 Call [QueryInterface](../vs140/QueryInterface.md) on an `IDebugProperty3` interface to obtain this interface.  
  
## Methods in Vtable order  
 The `IPropertyProxyProvider` interface implements the following method:  
  
|Method|Description|  
|------------|-----------------|  
|[IPropertyProxyProvider::GetPropertyProxy](../vs140/IPropertyProxyProvider--GetPropertyProxy.md)|Retrieves a property proxy interface to view data on an object.|  
  
## Remarks  
 Although the EE implements this interface, the implementation of [IPropertyProxyProvider::GetPropertyProxy](../vs140/IPropertyProxyProvider--GetPropertyProxy.md) is typically handled by [IEEVisualizerService::GetPropertyProxy](../vs140/IEEVisualizerService--GetPropertyProxy.md). See [Visualizing and Viewing Data](../vs140/Visualizing-and-Viewing-Data.md) for details on obtaining the IEEVisualizerService interface.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IEEVisualizerService::GetPropertyProxy](../vs140/IEEVisualizerService--GetPropertyProxy.md)   
 [Type Visualizer and Custom Viewer](../vs140/Type-Visualizer-and-Custom-Viewer.md)   
 [Visualizing and Viewing Data](../vs140/Visualizing-and-Viewing-Data.md)