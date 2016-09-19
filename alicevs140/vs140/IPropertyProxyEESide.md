---
title: "IPropertyProxyEESide"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cf227cf8-39d9-4758-8f7e-a697aebb1926
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IPropertyProxyEESide
This interface provides methods to view data on the associated object. This interface is part of the support for type visualizers.  
  
## Syntax  
  
```  
IPropertyProxyEESide : IUnknown  
```  
  
## Notes for Implementers  
 An expression evaluator implements this interface to support type visualizers.  
  
## Notes for Callers  
 Call [IPropertyProxyProvider::GetPropertyProxy](../vs140/IPropertyProxyProvider--GetPropertyProxy.md) to obtain this interface. Call [QueryInterface](../vs140/QueryInterface.md) on an [IDebugProperty3](../vs140/IDebugProperty3.md) interface to obtain the [IPropertyProxyProvider](../vs140/IPropertyProxyProvider.md) interface.  
  
## Methods in Vtable order  
 The following methods are implemented by this interface:  
  
|Method|Description|  
|------------|-----------------|  
|[InitSourceDataProvider](../vs140/IPropertyProxyEESide--InitSourceDataProvider.md)|Initializes a data source provider so that the object's data can be accessed.|  
|[GetManagedViewerCreationData](../vs140/IPropertyProxyEESide--GetManagedViewerCreationData.md)|Retrieves information about the object's assembly.|  
|[GetInitialData](../vs140/IPropertyProxyEESide--GetInitialData.md)|Gets the initial data for the object.|  
|[CreateReplacementObject](../vs140/IPropertyProxyEESide--CreateReplacementObject.md)|Creates a copy of an existing data storage.|  
|[InPlaceUpdateObject](../vs140/IPropertyProxyEESide--InPlaceUpdateObject.md)|Creates a reference to an existing data storage.|  
|[ResolveAssemblyRef](../vs140/IPropertyProxyEESide--ResolveAssemblyRef.md)|Retrieves information about a specific assembly in context of the assembly containing this object.|  
  
## Remarks  
 A type visualizer uses this interface to access the values associated with the object that this interface is part of. The data is accessed through the [IEEDataStorage](../vs140/IEEDataStorage.md) interface, which provides a read-only view of the data.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [Type Visualizer and Custom Viewer](../vs140/Type-Visualizer-and-Custom-Viewer.md)   
 [IEEDataStorage](../vs140/IEEDataStorage.md)   
 [IDebugObject](../vs140/IDebugObject.md)