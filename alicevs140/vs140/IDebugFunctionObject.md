---
title: "IDebugFunctionObject"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8d94e97c-a9d1-400c-8a98-a44b5385b33a
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugFunctionObject
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 This interface represents a function.  
  
## Syntax  
  
```  
IDebugFunctionObject : IDebugObject  
```  
  
## Notes for Implementers  
 An expression evaluator implements this interface to represent a function.  
  
## Notes for Callers  
 This interface is a specialization of the [IDebugObject](../vs140/IDebugObject.md) interface and is obtained using [QueryInterface](../vs140/QueryInterface.md) on the `IDebugObject` interface.  
  
## Methods in Vtable Order  
 In addition to the methods inherited from [IDebugObject](../vs140/IDebugObject.md), the `IDebugFunctionObject` interface exposes the following methods.  
  
|Method|Description|  
|------------|-----------------|  
|[CreatePrimitiveObject](../vs140/IDebugFunctionObject--CreatePrimitiveObject.md)|Creates a primitive data object.|  
|[CreateObject](../vs140/IDebugFunctionObject--CreateObject.md)|Creates an object using a constructor.|  
|[CreateObjectNoConstructor](../vs140/IDebugFunctionObject--CreateObjectNoConstructor.md)|Creates an object with no constructor.|  
|[CreateArrayObject](../vs140/IDebugFunctionObject--CreateArrayObject.md)|Creates an array object.|  
|[CreateStringObject](../vs140/IDebugFunctionObject--CreateStringObject.md)|Creates a string object.|  
|[Evaluate](../vs140/IDebugFunctionObject--Evaluate.md)|Calls the function and returns the resulting value as an object.|  
  
## Remarks  
 This interface enables the expression evaluator to represent functions in a parse tree. The `Create` methods in this interface are used to construct objects representing the input parameters to the method. The function can then be executed by calling the [Evaluate](../vs140/IDebugFunctionObject--Evaluate.md) method, which returns an object representing the return value of the function.  
  
## Requirements  
 Header: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Expression Evaluation Interfaces](../vs140/Expression-Evaluation-Interfaces.md)   
 [IDebugObject](../vs140/IDebugObject.md)