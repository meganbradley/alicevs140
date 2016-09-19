---
title: "Key Expression Evaluator Interfaces"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1cac9aa3-0867-4e12-a16e-1e90abbc0fb6
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Key Expression Evaluator Interfaces
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 When writing an expression evaluator (EE), along with the evaluation context, you should be familiar with the following interfaces.  
  
## Interface Descriptions  
  
-   [IDebugAddress](../vs140/IDebugAddress.md)  
  
     Has a single method, [IDebugAddress::GetAddress](../vs140/IDebugAddress--GetAddress.md), which gets a data structure that represents the current point of execution. This data structure is one of the three arguments that the debug engine (DE) passes to the [EvaluateSync](../vs140/IDebugParsedExpression--EvaluateSync.md) method to evaluate an expression. This interface is typically implemented by the symbol provider.  
  
-   [IDebugBinder](../vs140/IDebugBinder.md)  
  
     Has the [Bind](../vs140/IDebugBinder--Bind.md) method, which gets the memory area that contains the current value of a symbol. Given both the containing method, represented by an [IDebugObject](../vs140/IDebugObject.md) object, and the symbol itself, represented by an [IDebugField](../vs140/IDebugField.md) object, `IDebugBinder::Bind` returns the value of the symbol. `IDebugBinder` is typically implemented by the DE.  
  
-   [IDebugField](../vs140/IDebugField.md)  
  
     Represents a simple data type. For more complex types, such as arrays and methods, use the derived [IDebugArrayField](../vs140/IDebugArrayField.md) and [IDebugMethodField](../vs140/IDebugMethodField.md) interfaces, respectively. [IDebugContainerField](../vs140/IDebugContainerField.md) is another important derived interface that represents symbols containing other symbols, like methods or classes. The `IDebugField` interface (and its derivatives) is typically implemented by the symbol provider.  
  
     An `IDebugField` object can be used to find the name and type of a symbol and, together with an [IDebugBinder](../vs140/IDebugBinder.md) object, can be used to find its value.  
  
-   [IDebugObject](../vs140/IDebugObject.md)  
  
     Represents the actual bits of the run-time value of a symbol. [Bind](../vs140/IDebugBinder--Bind.md) takes an [IDebugField](../vs140/IDebugField.md) object, which represents a symbol, and returns an [IDebugObject](../vs140/IDebugObject.md) object. The [GetValue](../vs140/IDebugObject--GetValue.md) method returns the value of the symbol in a memory buffer. A DE typically implements this interface to represent the value of a property in memory.  
  
-   [IDebugExpressionEvaluator](../vs140/IDebugExpressionEvaluator.md)  
  
     This interface represents the expression evaluator itself. The key method is [IDebugExpressionEvaluator::Parse](../vs140/IDebugExpressionEvaluator--Parse.md), which returns an [IDebugParsedExpression](../vs140/IDebugParsedExpression.md) interface.  
  
-   [IDebugParsedExpression](../vs140/IDebugParsedExpression.md)  
  
     This interface represents a parsed expression ready to be evaluated. The key method is [IDebugParsedExpression::EvaluateSync](../vs140/IDebugParsedExpression--EvaluateSync.md) which returns an IDebugProperty2 representing the value and type of the expression.  
  
-   [IDebugProperty2](../vs140/IDebugProperty2.md)  
  
     This interface represents a value and its type and is the result of an expression evaluation.  
  
## See Also  
 [Evaluation Context](../vs140/Evaluation-Context.md)