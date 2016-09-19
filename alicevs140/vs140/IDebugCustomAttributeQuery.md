---
title: "IDebugCustomAttributeQuery"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b804b619-70eb-4c38-80d9-c8b32b65ed3e
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCustomAttributeQuery
Represents a query for custom attributes on a method or type.  
  
## Syntax  
  
```  
IDebugCustomAttributeQuery : IUnknown  
```  
  
## Methods  
 This interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugCustomAttributeQuery::GetCustomAttributeByName](../vs140/IDebugCustomAttributeQuery--GetCustomAttributeByName.md)|Retrieves a custom attribute given its name.|  
|[IDebugCustomAttributeQuery::IsCustomAttributeDefined](../vs140/IDebugCustomAttributeQuery--IsCustomAttributeDefined.md)|Determines in the specified custom attribute is defined.|  
  
## Requirements  
 Header: Sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll