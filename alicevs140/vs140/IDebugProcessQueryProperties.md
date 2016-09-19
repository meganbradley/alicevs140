---
title: "IDebugProcessQueryProperties"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ce29a248-81a0-42c0-99a7-1606e8c548ec
caps.latest.revision: 6
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcessQueryProperties
This interface is an extension interface implemented by [IDebugProcess2](../vs140/IDebugProcess2.md) implementers. It allows the implementer to get information on the debugging process environment.  
  
## Syntax  
  
```  
IDebugProcessQueryProperties: IUnknown  
```  
  
## Notes for Implementers  
 Implement this interface to get information on the execution environment of a debugging process.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugProcessQueryProperties`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugProcessQueryProperties::QueryProperty](../vs140/IDebugProcessQueryProperties--QueryProperty.md)|Queries for a property value.|  
|[IDebugProcessQueryProperties::QueryProperties](../vs140/IDebugProcessQueryProperties--QueryProperties.md)|Queries for property values.|  
  
## Remarks  
 This interface is seldom implemented.  
  
## Requirements  
 Header: Portpriv.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugProcess2](../vs140/IDebugProcess2.md)