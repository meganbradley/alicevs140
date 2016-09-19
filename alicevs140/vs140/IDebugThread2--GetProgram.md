---
title: "IDebugThread2::GetProgram"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8c9c5ea1-2031-472e-bc8f-30e22e754566
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugThread2::GetProgram
Gets the program in which a thread is running.  
  
## Syntax  
  
```cpp#  
HRESULT GetProgram (   
   IDebugProgram2** ppProgram  
);  
```  
  
```c#  
int GetProgram (   
   out IDebugProgram2 ppProgram  
);  
```  
  
#### Parameters  
 `ppProgram`  
 [out] Returns an [IDebugProgram2](../vs140/IDebugProgram2.md) object that represents the program this thread is running in.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugThread2](../vs140/IDebugThread2.md)   
 [IDebugProgram2](../vs140/IDebugProgram2.md)