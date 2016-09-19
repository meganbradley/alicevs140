---
title: "IDebugPortPicker"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8b7f6685-a3c5-4355-b706-c1b574f6ff84
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPortPicker
Represents a customized UI for selecting the port.  
  
## Syntax  
  
```  
IDebugPortPicker : IUnknown  
```  
  
## Notes for Implementers  
 This interface is implemented by port suppliers. A port supplier defines their port picker by exposing it as a CLSID and pointing the `metricPortPickerCLSID` metric at the exposed CLSID.  
  
## Methods  
 The following table shows the methods of `IDebugPortPicker`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugPortPicker::DisplayPortPicker](../vs140/IDebugPortPicker--DisplayPortPicker.md)|Displays the specified dialog box that allows the user to select a port.|  
|[IDebugPortPicker::SetSite](../vs140/IDebugPortPicker--SetSite.md)|Sets the service provider.|  
  
## Requirements  
 Header: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll