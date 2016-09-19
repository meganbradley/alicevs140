---
title: "IDebugThread2::Resume"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 36aad682-b0b9-40a2-b3fc-f0e61d41cdbc
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugThread2::Resume
Resumes execution of a thread.  
  
## Syntax  
  
```cpp#  
HRESULT Resume (   
   DWORD *pdwSuspendCount  
);  
```  
  
```c#  
int Resume (   
   out uint pdwSuspendCount  
);  
```  
  
#### Parameters  
 `pdwSuspendCount`  
 [out] Returns the suspend count after the resume operation.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Each call to this method decrements the suspend count until it reaches 0 at which time, execution is actually resumed. This suspend count is displayed in the **Threads** debug window.  
  
 For each call to this method, there must be a previous call to the [IDebugThread2::Suspend](../vs140/IDebugThread2--Suspend.md) method. The suspend count determines how many times the `IDebugThread2::Suspend` method has been called so far.  
  
## See Also  
 [IDebugThread2](../vs140/IDebugThread2.md)   
 [IDebugThread2::Suspend](../vs140/IDebugThread2--Suspend.md)