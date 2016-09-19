---
title: "IDebugArrayObject2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: be6e504d-4ab3-4141-a61b-0953ee0e038e
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugArrayObject2
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Represents a managed array object, and allows an expression evaluator (EE) to determine the base index (lower bounds) for the array.  
  
## Syntax  
  
```  
IDebugArrayObject2 : IDebugArrayObject  
```  
  
## Notes for Implementers  
 This is implemented by the managed debug engine (DE).  
  
## Methods  
 In addition to the methods on the [IDebugArrayObject](../vs140/IDebugArrayObject.md) interface, this interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugArrayObject2::GetBaseIndices](../vs140/IDebugArrayObject2--GetBaseIndices.md)|Retrieves the base indices (lower bounds) for each index given the number of dimensions in the array.|  
|[IDebugArrayObject2::HasBaseIndices](../vs140/IDebugArrayObject2--HasBaseIndices.md)|Determines if the array has base indices (lower bounds) defined.|  
  
## Remarks  
 An expression evaluator uses this interface to represent managed arrays in a parse tree.  
  
## Requirements  
 Header: Ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll