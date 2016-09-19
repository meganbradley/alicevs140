---
title: "IDiaAddressMap"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e6467529-508c-4328-85d7-89444ae4d1c1
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaAddressMap
Provides control over how the DIA SDK computes virtual and relative virtual addresses for debug objects.  
  
## Syntax  
  
```  
IDiaAddressMap : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaAddressMap`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaAddressMap::get_addressMapEnabled](../vs140/IDiaAddressMap--get_addressMapEnabled.md)|Indicates whether an address map has been established for a particular session.|  
|[IDiaAddressMap::put_addressMapEnabled](../vs140/IDiaAddressMap--put_addressMapEnabled.md)|Specifies whether the address map should be used to translate symbol addresses.|  
|[IDiaAddressMap::get_relativeVirtualAddressEnabled](../vs140/IDiaAddressMap--get_relativeVirtualAddressEnabled.md)|Indicates whether the calculation and use of relative virtual addresses is enabled.|  
|[IDiaAddressMap::put_relativeVirtualAddressEnabled](../vs140/IDiaAddressMap--put_relativeVirtualAddressEnabled.md)|Allows the client to enable or disable the calculation of relative virtual addresses.|  
|[IDiaAddressMap::get_imageAlign](../vs140/IDiaAddressMap--get_imageAlign.md)|Retrieves the current image alignment.|  
|[IDiaAddressMap::put_imageAlign](../vs140/IDiaAddressMap--put_imageAlign.md)|Sets the image alignment.|  
|[IDiaAddressMap::set_imageHeaders](../vs140/IDiaAddressMap--set_imageHeaders.md)|Sets image headers to enable the translation of relative virtual addresses.|  
|[IDiaAddressMap::set_addressMap](../vs140/IDiaAddressMap--set_addressMap.md)|Provides an address map to support image layout translations.|  
  
## Remarks  
 The control provided by this interface is encapsulated in two sets of data you supply: image headers and address maps. Most clients use the [IDiaDataSource::loadDataForExe](../vs140/IDiaDataSource--loadDataForExe.md) method to find the proper debug information for an image and the method can typically discover all of the necessary headers and maps data itself. However some clients implement specialized processing and searching for data. Such clients use the methods of the `IDiaAddressMap` interface to provide the DIA SDK with the search results.  
  
## Notes for Callers  
 This interface is available from the DIA session object. The client calls the `QueryInterface` method on DIA session object interface, usually [IDiaSession](../vs140/IDiaSession.md), to retrieve the `IDiaAddressMap` interface.  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../vs140/Interfaces--Debug-Interface-Access-SDK-.md)   
 [IDiaDataSource::loadDataForExe](../vs140/IDiaDataSource--loadDataForExe.md)   
 [IDiaSession](../vs140/IDiaSession.md)