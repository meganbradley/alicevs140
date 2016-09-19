---
title: "IDebugExpressionEvaluator2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cebe649f-1c77-4d33-854f-30d4f00eceb4
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugExpressionEvaluator2
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Represents an enhanced version of an expression evaluator (EE).  
  
## Syntax  
  
```  
IDebugExpressionEvaluator2 : IDebugExpressionEvaluator  
```  
  
## Notes for Implementers  
 This interface is implemented by an expression evaluator.  
  
## Methods  
 In addition to the methods on the [IDebugExpressionEvaluator](../vs140/IDebugExpressionEvaluator.md) interface, this interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugExpressionEvaluator2::GetService](../vs140/IDebugExpressionEvaluator2--GetService.md)|Retrieves a service object given its unique identifier.|  
|[IDebugExpressionEvaluator2::PreloadModules](../vs140/IDebugExpressionEvaluator2--PreloadModules.md)|Preloads the modules designated by the specified symbol provider.|  
|[IDebugExpressionEvaluator2::SetCallback](../vs140/IDebugExpressionEvaluator2--SetCallback.md)|Enables the expression evaluator (EE) to specify the callback interface the debugger engine (DE) will use to read metric settings.|  
|[IDebugExpressionEvaluator2::SetCorPath](../vs140/IDebugExpressionEvaluator2--SetCorPath.md)|Sets the path to the common language runtime (CLR) loaded in the debugger.|  
|[IDebugExpressionEvaluator2::SetIDebugIDECallback](../vs140/IDebugExpressionEvaluator2--SetIDebugIDECallback.md)|Enables a debug engine to pass a callback to the expression evaluator during initialization.|  
|[IDebugExpressionEvaluator2::Terminate](../vs140/IDebugExpressionEvaluator2--Terminate.md)|Stops and cleans up the expression evaluator.|  
  
## Requirements  
 Header: Ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll