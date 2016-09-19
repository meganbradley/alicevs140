---
title: "IDebugTypeFieldBuilder"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2dfed0be-6972-4bec-baec-f0b78df9ef97
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugTypeFieldBuilder
Represents the ability to create a field that represents a type.  
  
## Syntax  
  
```  
IDebugTypeFieldBuilder : IUnknown  
```  
  
## Notes for Callers  
 This interface is obtained from the symbol provider.  
  
## Methods  
 This interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugTypeFieldBuilder::CreatePrimitive](../vs140/IDebugTypeFieldBuilder--CreatePrimitive.md)|Creates an object that represents a primitive type.|  
|[IDebugTypeFieldBuilder::CreatePointerToType](../vs140/IDebugTypeFieldBuilder--CreatePointerToType.md)|Creates a pointer to the specified type.|  
  
## Requirements  
 Header: Sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll