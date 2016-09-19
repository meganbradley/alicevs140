---
title: "IDebugProcess2::EnumThreads"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 05677385-7a7f-4545-8438-af00dde85db0
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess2::EnumThreads
Retrieves a list of all the threads running in the process.  
  
## Syntax  
  
```cpp#  
HRESULT EnumThreads(  
   IEnumDebugThreads2** ppEnum  
);  
```  
  
```c#  
int EnumThreads(  
   out IEnumDebugThreads2 ppEnum  
);  
```  
  
#### Parameters  
 `ppEnum`  
 [out] Returns an [IEnumDebugThreads2](../vs140/IEnumDebugThreads2.md) object that contains a list of all threads in all programs in the process.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This method enumerates the threads running in each program and then combines them into a process view of the threads. A single thread may run in multiple programs; this method enumerates that thread only once.  
  
 This method presents a list of the process's threads without duplicates. Otherwise, to enumerate the threads running in a particular program, use the [EnumThreads](../vs140/IDebugProgram2--EnumThreads.md) method.  
  
## See Also  
 [IDebugProcess2](../vs140/IDebugProcess2.md)   
 [IEnumDebugThreads2](../vs140/IEnumDebugThreads2.md)   
 [IDebugThread2](../vs140/IDebugThread2.md)   
 [EnumThreads](../vs140/IDebugProgram2--EnumThreads.md)