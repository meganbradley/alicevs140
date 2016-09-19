---
title: "IDebugStackFrame2::GetExpressionContext"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a2604e6a-502d-473b-868f-b11ac64c7a35
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugStackFrame2::GetExpressionContext
Gets an evaluation context for expression evaluation within the current context of a stack frame and thread.  
  
## Syntax  
  
```cpp#  
HRESULT GetExpressionContext (   
   IDebugExpressionContext2** ppExprCxt  
);  
```  
  
```c#  
int GetExpressionContext (   
   out IDebugExpressionContext2 ppExprCxt  
);  
```  
  
#### Parameters  
 `ppExprCxt`  
 [out] Returns an [IDebugExpressionContext2](../vs140/IDebugExpressionContext2.md) object that represents a context for expression evaluation.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Generally, an expression evaluation context can be thought of as a scope for performing expression evaluation. Call the [IDebugExpressionContext2::ParseText](../vs140/IDebugExpressionContext2--ParseText.md) method to parse an expression and then call the resulting [IDebugExpression2::EvaluateSync](../vs140/IDebugExpression2--EvaluateSync.md) or [IDebugExpression2::EvaluateAsync](../vs140/IDebugExpression2--EvaluateAsync.md) methods to evaluate the parsed expression.  
  
## See Also  
 [IDebugStackFrame2](../vs140/IDebugStackFrame2.md)   
 [IDebugExpressionContext2](../vs140/IDebugExpressionContext2.md)   
 [IDebugExpressionContext2::ParseText](../vs140/IDebugExpressionContext2--ParseText.md)   
 [IDebugExpression2::EvaluateSync](../vs140/IDebugExpression2--EvaluateSync.md)   
 [IDebugExpression2::EvaluateAsync](../vs140/IDebugExpression2--EvaluateAsync.md)