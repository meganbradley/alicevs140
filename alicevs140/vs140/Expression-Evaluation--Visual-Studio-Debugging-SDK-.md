---
title: "Expression Evaluation (Visual Studio Debugging SDK)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5044ced5-c18c-4534-b0bf-cc3e50cd57ac
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Expression Evaluation (Visual Studio Debugging SDK)
During break mode, the IDE must be able to evaluate simple expressions involving several variables of your program. To accomplish this, the debug engine (DE) must be able to parse and evaluate an expression that is entered into one of the windows of the IDE.  
  
 Expressions are created using the [IDebugExpressionContext2::ParseText](../vs140/IDebugExpressionContext2--ParseText.md) method and are represented by the resulting [IDebugExpression2](../vs140/IDebugExpression2.md) interface.  
  
 The **IDebugExpression2** interface is implemented by the DE and calls its **EvalAsync** method to return an [IDebugProperty2](../vs140/IDebugProperty2.md) interface to the IDE, in order to display the results of the expression evaluation in the IDE. [IDebugProperty2::GetPropertyInfo](../vs140/IDebugProperty2--GetPropertyInfo.md) returns a structure that can be used to put the value of an expression into a Watch window or into the Locals window.  
  
 The debug package or session debug manager (SDM) calls [IDebugExpression2::EvaluateAsync](../vs140/IDebugExpression2--EvaluateAsync.md) or [EvaluateSync](../vs140/IDebugExpression2--EvaluateSync.md) to get an [IDebugProperty2](../vs140/IDebugProperty2.md) interface that represents the result of the evaluation. `IDebugProperty2` has methods that return the name, type, and value of the expression. This information is displayed in various debugger windows.  
  
## Using Expression Evaluation  
 To use expression evaluation, you must implement the [IDebugExpressionContext2::ParseText](../vs140/IDebugExpressionContext2--ParseText.md) method and all of the methods of the [IDebugExpression2](../vs140/IDebugExpression2.md) interface, as shown in the following table.  
  
|Method|Description|  
|------------|-----------------|  
|[EvaluateAsync](../vs140/IDebugExpression2--EvaluateAsync.md)|Evaluates an expression asynchronously.|  
|[Abort](../vs140/IDebugExpression2--Abort.md)|Ends asynchronous expression evaluation.|  
|[EvaluateSync](../vs140/IDebugExpression2--EvaluateSync.md)|Evaluates an expression synchronously.|  
  
 Synchronous and asynchronous evaluation require the implementation of the [IDebugProperty2::GetPropertyInfo](../vs140/IDebugProperty2--GetPropertyInfo.md) method. Asynchronous expression evaluation requires the implementation of [IDebugExpressionEvaluationCompleteEvent2](../vs140/IDebugExpressionEvaluationCompleteEvent2.md).  
  
## See Also  
 [Execution Control and State Evaluation](../vs140/Execution-Control-and-State-Evaluation.md)