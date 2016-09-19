---
title: "IDebugParsedExpression"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: be6486ed-b070-4898-95b1-58581bcb4447
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugParsedExpression
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 This interface represents a parsed expression ready to be evaluated.  
  
## Syntax  
  
```  
IDebugParsedExpression : IUnknown  
```  
  
## Notes for Implementers  
 An expression evaluator implements this interface to represent a parsed expression that is ready for evaluation.  
  
## Notes for Callers  
 A call to [IDebugExpressionEvaluator::Parse](../vs140/IDebugExpressionEvaluator--Parse.md) returns this interface.  
  
## Methods in Vtable Order  
 The following table shows the method of `IDebugParsedExpression`.  
  
|Method|Description|  
|------------|-----------------|  
|[EvaluateSync](../vs140/IDebugParsedExpression--EvaluateSync.md)|Evaluates the parsed expression.|  
  
## Remarks  
 When the caller is ready to evaluate the expression, it calls [IDebugParsedExpression::EvaluateSync](../vs140/IDebugParsedExpression--EvaluateSync.md) to return an [IDebugProperty2](../vs140/IDebugProperty2.md) that contains the result of the evaluation. This two-part approach to evaluation, parsing then evaluating, enables the parsed expression to be evaluated multiple times, bypassing the time-consuming process of parsing the expression.  
  
## Requirements  
 Header: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Parse](../vs140/IDebugExpressionEvaluator--Parse.md)   
 [EvaluateSync](../vs140/IDebugParsedExpression--EvaluateSync.md)   
 [IDebugProperty2](../vs140/IDebugProperty2.md)