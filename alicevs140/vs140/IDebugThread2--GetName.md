---
title: "IDebugThread2::GetName"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eec54b8f-4a0e-4919-b0f9-81d4bd1e0b6f
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugThread2::GetName
Gets the name of a thread.  
  
## Syntax  
  
```cpp#  
HRESULT GetName (   
   BSTR* pbstrName  
);  
```  
  
```c#  
int GetName (   
   out string pbstrName  
);  
```  
  
#### Parameters  
 `pbstrName`  
 [out] Returns the name of the thread.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The retrieved name is always a name that can be displayed and this name describes the thread. The thread name might be derived from a run-time architecture that supports named threads, or it might be a name derived from the debug engine. Alternatively, the name of the thread can be set by a call to the [IDebugThread2::SetThreadName](../vs140/IDebugThread2--SetThreadName.md) method.  
  
## See Also  
 [IDebugThread2](../vs140/IDebugThread2.md)   
 [IDebugThread2::SetThreadName](../vs140/IDebugThread2--SetThreadName.md)