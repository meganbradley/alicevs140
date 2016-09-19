---
title: "IDebugPointerObject3"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 11d26af4-1079-435e-96fa-d5269cbea8eb
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPointerObject3
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Represents a pointer in a parse tree, and extends the **IDebugPointerObject** interface.  
  
## Syntax  
  
```  
IDebugPointerObject3 : IDebugPointerObject  
```  
  
## Notes for Implementers  
 An expression evaluator (EE) implements this interface.  
  
## Methods  
 In addition to the methods on the [IDebugPointerObject](../vs140/IDebugPointerObject.md) interface, this interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugPointerObject3::GetPointerAddress](../vs140/IDebugPointerObject3--GetPointerAddress.md)|Retrieves the address of pointer.|  
  
## Requirements  
 Header: Ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll