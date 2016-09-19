---
title: "IDebugFunctionObject2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 56b2fdff-146d-4138-a34c-59a9c65a3ddd
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugFunctionObject2
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Represents a function and enhances the [IDebugFunctionObject](../vs140/IDebugFunctionObject.md) interface.  
  
## Syntax  
  
```  
IDebugFunctionObject2 : IUnknown  
```  
  
## Notes for Implementers  
 An expression evaluator (EE) implements this interface to represent a function.  
  
## Notes for Callers  
 Methods of this interface defer those of **IDebugFunctionObject** in the following ways:  
  
-   The **IDebugEvaluate** method takes flags.  
  
-   The **CreateObject** method takes flags and a timeout.  
  
-   The **CreateStringObjectWithLength** method takes a length.  
  
## Methods  
 This interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugFunctionObject2::CreateObject](../vs140/IDebugFunctionObject2--CreateObject.md)|Creates an object that uses a constructor given evaluation flag settings and a timeout value.|  
|[IDebugFunctionObject2::CreateStringObjectWithLength](../vs140/IDebugFunctionObject2--CreateStringObjectWithLength.md)|Creates a string object that has the specified length.|  
|[IDebugFunctionObject2::Evaluate](../vs140/IDebugFunctionObject2--Evaluate.md)|Calls the function and returns the resulting value as an object.|  
  
## Requirements  
 Header: Ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll