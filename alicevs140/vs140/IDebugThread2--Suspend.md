---
title: "IDebugThread2::Suspend"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1e20be85-aa12-48de-bb83-0bf0976e99ae
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugThread2::Suspend
Suspends a thread.  
  
## Syntax  
  
```cpp#  
HRESULT Suspend (   
   DWORD *pdwSuspendCount  
);  
```  
  
```c#  
HRESULT Suspend (   
   out uint pdwSuspendCount  
);  
```  
  
#### Parameters  
 `pdwSuspendCount`  
 [out] Returns the suspend count after the suspend operation.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Each call to this method increments the suspend count above 0. This suspend count is displayed in the **Threads** debug window.  
  
 For each call to this method, there must be a later call to the [IDebugThread2::Resume](../vs140/IDebugThread2--Resume.md) method.  
  
## See Also  
 [IDebugThread2](../vs140/IDebugThread2.md)   
 [IDebugThread2::Resume](../vs140/IDebugThread2--Resume.md)