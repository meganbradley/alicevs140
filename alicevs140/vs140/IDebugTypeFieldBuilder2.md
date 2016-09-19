---
title: "IDebugTypeFieldBuilder2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 23911c5b-2bbf-4734-9976-87a0bd6ea36c
caps.latest.revision: 8
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugTypeFieldBuilder2
Extends the **IDebugTypeFieldBuilder** to be able to create array types.  
  
## Syntax  
  
```  
IDebugTypeFieldBuilder2 : IDebugTypeFieldBuilder  
```  
  
## Notes for Callers  
 This interface can be obtained from the symbol provider.  
  
## Methods  
 In addition to the methods on the [IDebugTypeFieldBuilder](../vs140/IDebugTypeFieldBuilder.md) interface, this interface implements the following method:  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugTypeFieldBuilder2::CreateArrayOfType](../vs140/IDebugTypeFieldBuilder2--CreateArrayOfType.md)|Creates an array of the specified type and size.|  
  
## Requirements  
 Header: Sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll