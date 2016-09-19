---
title: "IDebugExpressionEvaluationCompleteEvent2::GetResult"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d9ad3e22-b6b2-421e-9a43-6bb8c70d12a9
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugExpressionEvaluationCompleteEvent2::GetResult
Gets the result of expression evaluation.  
  
## Syntax  
  
```cpp#  
HRESULT GetResult(   
   IDebugProperty2** ppResult  
);  
```  
  
```c#  
int GetResult(   
   out IDebugProperty2 ppResult  
);  
```  
  
#### Parameters  
 `ppResult`  
 [out] Returns an [IDebugProperty2](../vs140/IDebugProperty2.md) object that represents the result of the expression evaluation.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The returned [IDebugProperty2](../vs140/IDebugProperty2.md) object contains the value of the evaluated expression. Note that this value could be a complex value such as an array but the final result must be a numerical or string value that is displayed to the user.  
  
## See Also  
 [IDebugExpressionEvaluationCompleteEvent2](../vs140/IDebugExpressionEvaluationCompleteEvent2.md)   
 [IDebugProperty2](../vs140/IDebugProperty2.md)