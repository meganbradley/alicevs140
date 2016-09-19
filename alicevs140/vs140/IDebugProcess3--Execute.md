---
title: "IDebugProcess3::Execute"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d831cd81-d7bf-4172-8517-aa699867791f
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess3::Execute
Continues running this process from a stopped state. Any previous execution state (such as a step) is cleared and the process starts executing again.  
  
> [!NOTE]
>  This method should be used instead of [IDebugProgram2::Execute](../vs140/IDebugProgram2--Execute.md).  
  
## Syntax  
  
```cpp  
HRESULT Execute(  
   IDebugThread2* pThread  
);  
```  
  
```c#  
int Execute(  
   IDebugThread2 pThread  
);  
```  
  
#### Parameters  
 `pThread`  
 [in] An [IDebugThread2](../vs140/IDebugThread2.md) object representing the thread to execute.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns error code.  
  
## Remarks  
 When the user starts execution from a stopped state in some other process's thread, this method is called on this process. This method is also called when the user selects the **Start** command from the **Debug** menu in the IDE. The implementation of this method may be as simple as calling the [IDebugThread2::Resume](../vs140/IDebugThread2--Resume.md) method on the current thread in the process.  
  
> [!WARNING]
>  Do not send a stopping event or an immediate (synchronous) event to [IDebugEventCallback2::Event](../vs140/IDebugEventCallback2--Event.md) while handling this call; otherwise the debugger may hang.  
  
## See Also  
 [IDebugProcess3](../vs140/IDebugProcess3.md)   
 [IDebugThread2](../vs140/IDebugThread2.md)   
 [IDebugThread2::Resume](../vs140/IDebugThread2--Resume.md)   
 [IDebugEventCallback2::Event](../vs140/IDebugEventCallback2--Event.md)