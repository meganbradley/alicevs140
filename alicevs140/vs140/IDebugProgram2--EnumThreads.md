---
title: "IDebugProgram2::EnumThreads"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0f2a8c51-1315-4c96-8aa1-6a937dc2a769
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgram2::EnumThreads
Retrieves a list of the threads that are running in the program.  
  
## Syntax  
  
```cpp#  
HRESULT EnumThreads(   
   IEnumDebugThreads2** ppEnum  
);  
```  
  
```c#  
int EnumThreads(   
   out IEnumDebugThreads2 ppEnum  
);  
```  
  
#### Parameters  
 `ppEnum`  
 [out] Returns an [IEnumDebugThreads2](../vs140/IEnumDebugThreads2.md) object that contains a list of the threads.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugProgram2](../vs140/IDebugProgram2.md)   
 [IEnumDebugThreads2](../vs140/IEnumDebugThreads2.md)   
 [IDebugThread2](../vs140/IDebugThread2.md)