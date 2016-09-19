---
title: "IDebugExpressionEvaluator2::SetIDebugIDECallback"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f01c40ad-ef4b-477b-8304-602c6972bc88
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugExpressionEvaluator2::SetIDebugIDECallback
Enables a debug engine to pass a callback to the expression evaluator during initialization.  
  
## Syntax  
  
```cpp#  
HRESULT SetIDebugIDECallback (  
   IDebugIDECallback * pCallback  
);  
```  
  
```c#  
int SetIDebugIDECallback (  
   IDebugIDECallback pCallback  
);  
```  
  
#### Parameters  
 `pCallback`  
 [in] Interface for the callback.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugExpressionEvaluator2](../vs140/IDebugExpressionEvaluator2.md)