---
title: "IDebugModule3::SetJustMyCodeState"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 68f8166d-ef64-49ae-ad5e-79604f43bbd4
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugModule3::SetJustMyCodeState
Marks the module as being user code or not.  
  
## Syntax  
  
```cpp#  
HRESULT SetJustMyCodeState(  
   BOOL fIsUserCode  
);  
```  
  
```c#  
int SetJustMyCodeState(  
   int fIsUserCode  
);  
```  
  
#### Parameters  
 `fIsUserCode`  
 [in] Nonzero (`TRUE`) if the module should be considered user code, zero (`FALSE`) if it should not.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns error code.  
  
## See Also  
 [IDebugModule3](../vs140/IDebugModule3.md)