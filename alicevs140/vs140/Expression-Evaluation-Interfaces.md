---
title: "Expression Evaluation Interfaces"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2d259f60-2cd7-460e-b02d-24a8fb202850
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Expression Evaluation Interfaces
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 The following are the Expression Evaluation Interfaces for the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Debugging SDK.  
  
## Discussion  
 These interfaces are used to evaluate expressions in a call stack during break mode. They are implemented only for common language run-time expression evaluators (EE).  
  
 Each interface in the table shows the component that can implement it from the following list:  
  
-   Debug Engine (DE)  
  
-   Expression Evaluator (EE)  
  
-   Visual Studio (VS)  
  
|Interface|Implemented by|Description|  
|---------------|--------------------|-----------------|  
|[IDebugAlias](../vs140/IDebugAlias.md)|EE|Represents a numeric alias for a variable.|  
|[IDebugAlias2](../vs140/IDebugAlias2.md)|EE|Represents a numeric alias for a variable, and enables an expression evaluator (EE) to obtain the application domain for the alias.|  
|[IDebugArrayObject](../vs140/IDebugArrayObject.md)|EE|Represents an array object.|  
|[IDebugArrayObject2](../vs140/IDebugArrayObject2.md)|EE|Represents a managed array object, and allows an expression evaluator (EE) to determine the base index (lower bounds) for the array.|  
|[IDebugBinder](../vs140/IDebugBinder.md)|DE|Represents a binder that binds debug symbols to actual addresses in memory.|  
|[IDebugBinder3](../vs140/IDebugBinder3.md)|DE|Same as the [IDebugBinder](../vs140/IDebugBinder.md) interface but provides access to types, aliases, and custom visualizers.|  
|[IDebugExpressionEvaluator](../vs140/IDebugExpressionEvaluator.md)|EE|Represents the expression evaluator.|  
|[IDebugExpressionEvaluator2](../vs140/IDebugExpressionEvaluator2.md)|EE|Represents an enhanced version of an expression evaluator (EE).|  
|[IDebugExpressionEvaluator3](../vs140/IDebugExpressionEvaluator3.md)|EE|Represents an expression evaluator (EE) with an enhanced parser tree.|  
|[IDebugFunctionObject](../vs140/IDebugFunctionObject.md)|EE|Represents a function.|  
|[IDebugFunctionObject2](../vs140/IDebugFunctionObject2.md)|EE|Represents a function and enhances the [IDebugFunctionObject](../vs140/IDebugFunctionObject.md) interface.|  
|[IDebugIDECallback](../vs140/IDebugIDECallback.md)|DE|Enables an expression evaluator (EE) to display a message in the debugger's output window.|  
|[IDebugManagedObject](../vs140/IDebugManagedObject.md)|EE|Represents a managed code object.|  
|[IDebugObject](../vs140/IDebugObject.md)|EE|Base interface that represents any symbol bound to a memory address.|  
|[IDebugObject2](../vs140/IDebugObject2.md)|EE|Same as the [IDebugObject](../vs140/IDebugObject.md) interface but provides access to additional information.|  
|[IDebugParsedExpression](../vs140/IDebugParsedExpression.md)|EE|Represents a parsed expression ready to be evaluated.|  
|[IDebugPointerObject](../vs140/IDebugPointerObject.md)|EE|Represents a pointer.|  
|[IDebugPointerObject3](../vs140/IDebugPointerObject3.md)|EE|Represents a pointer in a parse tree, and extends the **IDebugPointerObject** interface.|  
|[IEEVisualizerDataProvider](../vs140/IEEVisualizerDataProvider.md)|EE|Provides the ability to modify a type's value through a type visualizer.|  
|[IEEVisualizerService](../vs140/IEEVisualizerService.md)|VS|Provides access to custom viewers and type visualizers.|  
|[IEEVisualizerServiceProvider](../vs140/IEEVisualizerServiceProvider.md)|VS|Provides the ability to create an [IEEVisualizerService](../vs140/IEEVisualizerService.md) object.|  
|[IEnumDebugObjects](../vs140/IEnumDebugObjects.md)|EE|Represents a collection of [IDebugObject](../vs140/IDebugObject.md) objects.|  
  
## See Also  
 [API Reference](../vs140/API-Reference--Visual-Studio-Debugging-.md)   
 [Writing a CLR Expression Evaluator](../vs140/Writing-a-Common-Language-Runtime-Expression-Evaluator.md)   
 [Type Visualizer and Custom Viewer](../vs140/Type-Visualizer-and-Custom-Viewer.md)