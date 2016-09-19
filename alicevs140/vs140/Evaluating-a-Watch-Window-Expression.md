---
title: "Evaluating a Watch Window Expression"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b07e72c7-60d3-4b30-8e3f-6db83454c348
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Evaluating a Watch Window Expression
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 When execution pauses, Visual Studio calls the debug engine (DE) to determine the current value of each expression in its watch list. The DE evaluates each expression using an expression evaluator (EE), and Visual Studio displays its value in the **Watch** window.  
  
 Here is an overview of how a watch list expression is evaluated:  
  
1.  Visual Studio calls the DE's [IDebugStackFrame2::GetExpressionContext](../vs140/IDebugStackFrame2--GetExpressionContext.md) to get an expression context that can be used to evaluate expressions.  
  
2.  For each expression in the watch list, Visual Studio calls [IDebugExpressionContext2::ParseText](../vs140/IDebugExpressionContext2--ParseText.md) to convert the expression text into a parsed expression.  
  
3.  `IDebugExpressionContext2::ParseText` calls [IDebugExpressionEvaluator::Parse](../vs140/IDebugExpressionEvaluator--Parse.md) to do the actual work of parsing the text and produce an [IDebugParsedExpression](../vs140/IDebugParsedExpression.md) object.  
  
4.  `IDebugExpressionContext2::ParseText` creates an [IDebugExpression2](../vs140/IDebugExpression2.md) object and puts the `IDebugParsedExpression` object into it. This I`DebugExpression2` object is then returned to Visual Studio.  
  
5.  Visual Studio calls [IDebugExpression2::EvaluateSync](../vs140/IDebugExpression2--EvaluateSync.md) to evaluate the parsed expression.  
  
6.  `IDebugExpression2::EvaluateSync` passes the call to [IDebugParsedExpression::EvaluateSync](../vs140/IDebugParsedExpression--EvaluateSync.md) to do the actual evaluation and produce an [IDebugProperty2](../vs140/IDebugProperty2.md) object that is returned to Visual Studio.  
  
7.  Visual Studio calls [IDebugProperty2::GetPropertyInfo](../vs140/IDebugProperty2--GetPropertyInfo.md) to obtain the value of the expression that is then displayed in the watch list.  
  
## Parse Then Evaluate  
 Since parsing a complex expression can take much longer than evaluating it, the process of evaluating an expression is broken up into two steps: 1) parse the expression and 2) evaluate the parsed expression. This way, evaluation can occur many times but the expression needs to be parsed only once. The intermediate parsed expression is returned from the EE in an [IDebugParsedExpression](../vs140/IDebugParsedExpression.md) object that is in turn encapsulated and returned from the DE as an [IDebugExpression2](../vs140/IDebugExpression2.md) object. The `IDebugExpression` object defers all evaluation to the `IDebugParsedExpression` object.  
  
> [!NOTE]
>  It is not necessary for an EE to adhere to this two-step process even though Visual Studio assumes this; the EE can parse and evaluate in the same step when [IDebugParsedExpression::EvaluateSync](../vs140/IDebugParsedExpression--EvaluateSync.md) is called (this is how the MyCEE sample works, for example). If your language can form complex expressions, you may want to separate the parse step from the evaluation step. This can increase performance in the Visual Studio debugger when many watch expressions are being shown.  
  
## In This Section  
 [Sample Implementation of Expression Evaluation](../vs140/Sample-Implementation-of-Expression-Evaluation.md)  
 Uses the MyCEE sample to step through the process of expression evaluation.  
  
 [Evaluating a Watch Expression](../vs140/Evaluating-a-Watch-Expression.md)  
 Explains what happens after a successful expression parse.  
  
## Related Sections  
 [Evaluation Context](../vs140/Evaluation-Context.md)  
 Provides the arguments that are passed when the debug engine (DE) calls the expression evaluator (EE).  
  
## See Also  
 [Writing a Common Language Run-time Expression Evaluator](../vs140/Writing-a-Common-Language-Runtime-Expression-Evaluator.md)