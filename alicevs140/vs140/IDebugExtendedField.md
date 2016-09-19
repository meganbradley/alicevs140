---
title: "IDebugExtendedField"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b491499c-af57-47da-87d6-34b7398f6591
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugExtendedField
Extends the types of fields that are available to support managed code generics.  
  
## Syntax  
  
```  
IDebugExtendedField : IDebugField  
```  
  
## Methods  
 In addition to the methods on the [IDebugField](../vs140/IDebugField.md) interface, this interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugExtendedField::GetExtendedKind](../vs140/IDebugExtendedField--GetExtendedKind.md)|Retrieves the specified extended field kind.|  
|[IDebugExtendedField::IsClosedType](../vs140/IDebugExtendedField--IsClosedType.md)|Determines if the field represents a closed type.|  
  
## Requirements  
 Header: Sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll