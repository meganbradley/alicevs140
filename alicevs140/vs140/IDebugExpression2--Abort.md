---
title: "IDebugExpression2::Abort"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4fcb712e-1bdb-4b75-a440-35cc79ee147e
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugExpression2::Abort
This method cancels asynchronous expression evaluation as started by a call to the [IDebugExpression2::EvaluateAsync](../vs140/IDebugExpression2--EvaluateAsync.md) method.  
  
## Syntax  
  
```cpp#  
HRESULT Abort(  
   void  
);  
```  
  
```c#  
int Abort();  
```  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 When asynchronous expression evaluation is cancelled, do not sent an [IDebugExpressionEvaluationCompleteEvent2](../vs140/IDebugExpressionEvaluationCompleteEvent2.md) event to the event callback passed to the [IDebugProgram2::Attach](../vs140/IDebugProgram2--Attach.md) or [IDebugEngine2::Attach](../vs140/IDebugEngine2--Attach.md) methods.  
  
## See Also  
 [IDebugExpression2](../vs140/IDebugExpression2.md)   
 [IDebugExpressionEvaluationCompleteEvent2](../vs140/IDebugExpressionEvaluationCompleteEvent2.md)   
 [IDebugExpression2::EvaluateAsync](../vs140/IDebugExpression2--EvaluateAsync.md)