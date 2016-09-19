---
title: "IDebugStackFrame2::GetThread"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cbeef85b-3dd7-4f97-adc2-c4d197d979fc
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugStackFrame2::GetThread
Gets the thread associated with a stack frame.  
  
## Syntax  
  
```cpp#  
HRESULT GetThread (   
   IDebugThread2** ppThread  
);  
```  
  
```c#  
int GetThread (   
   out IDebugThread2 ppThread  
);  
```  
  
#### Parameters  
 `ppThread`  
 [out] Returns an [IDebugThread2](../vs140/IDebugThread2.md) object that represents the thread.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugStackFrame2](../vs140/IDebugStackFrame2.md)   
 [IDebugThread2](../vs140/IDebugThread2.md)