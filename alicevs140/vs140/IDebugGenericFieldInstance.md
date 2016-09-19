---
title: "IDebugGenericFieldInstance"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f68b4761-be8b-4801-9d4b-cde90e01d95e
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugGenericFieldInstance
Represents an instance of a field for a managed code generic type.  
  
## Syntax  
  
```  
IDebugGenericFieldInstance : IUnknown  
```  
  
## Methods  
 This interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugGenericFieldInstance::GetTypeArguments](../vs140/IDebugGenericFieldInstance--GetTypeArguments.md)|Retrieves the type parameter arguments for this instance.|  
|[IDebugGenericFieldInstance::TypeArgumentCount](../vs140/IDebugGenericFieldInstance--TypeArgumentCount.md)|Returns the number of type parameter arguments for this instance.|  
  
## Requirements  
 Header: Sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll