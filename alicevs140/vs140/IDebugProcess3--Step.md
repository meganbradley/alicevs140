---
title: "IDebugProcess3::Step"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6ad9094c-27cc-4927-8a7c-1b4d97b2e436
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess3::Step
Causes the process to step one instruction or statement.  
  
> [!NOTE]
>  This method should be used instead of [IDebugProgram2::Step](../vs140/IDebugProgram2--Step.md).  
  
## Syntax  
  
```cpp  
HRESULT Step(  
   IDebugThread2* pThread,  
   STEPKIND       sk,  
   STEPUNIT       step,  
);  
```  
  
```c#  
int Step(  
   IDebugThread2 pThread,   
   enum_STEPKIND sk,   
   enum_STEPUNIT step  
);  
```  
  
#### Parameters  
 `pThread`  
 [in] An [IDebugThread2](../vs140/IDebugThread2.md) object representing the thread being stepped.  
  
 `sk`  
 [in] One of the [STEPKIND](../vs140/STEPKIND.md) values.  
  
 `step`  
 [in] One of the [STEPUNIT](../vs140/STEPUNIT.md) values.  
  
## Return Value  
 If successful, returns S_OK; otherwise returns error code.  
  
## Remarks  
 In case there is any thread synchronization or communication between threads, other threads in the process should run when a particular thread is stepping.  
  
 **Warning** Do not send a stopping event or an immediate (synchronous) event to [IDebugEventCallback2::Event](../vs140/IDebugEventCallback2--Event.md) while handling this call; otherwise the debugger may hang.  
  
## See Also  
 [IDebugProcess3](../vs140/IDebugProcess3.md)   
 [IDebugThread2](../vs140/IDebugThread2.md)   
 [STEPKIND](../vs140/STEPKIND.md)   
 [STEPUNIT](../vs140/STEPUNIT.md)   
 [IDebugEventCallback2::Event](../vs140/IDebugEventCallback2--Event.md)