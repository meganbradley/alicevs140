---
title: "IDebugProgram2::Execute"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f7205ce8-0ac6-4fcd-b6ec-b720b4fcaccf
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgram2::Execute
Continues running this program from a stopped state. Any previous execution state (such as a step) is cleared, and the program starts executing again.  
  
> [!NOTE]
>  This method is deprecated. Use the [IDebugProcess3::Execute](../vs140/IDebugProcess3--Execute.md) method instead.  
  
## Syntax  
  
```cpp#  
HRESULT Execute(  
   void  
);  
```  
  
```c#  
int Execute();  
```  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 When the user starts execution from a stopped state in some other program's thread, this method is called on this program. This method is also called when the user selects the **Start** command from the **Debug** menu in the IDE. The implementation of this method may be as simple as calling the [IDebugThread2::Resume](../vs140/IDebugThread2--Resume.md) method on the current thread in the program.  
  
> [!WARNING]
>  Do not send a stopping event or an immediate (synchronous) event to [IDebugEventCallback2::Event](../vs140/IDebugEventCallback2--Event.md) while handling this call; otherwise the debugger may hang.  
  
## See Also  
 [IDebugProgram2](../vs140/IDebugProgram2.md)   
 [IDebugEventCallback2::Event](../vs140/IDebugEventCallback2--Event.md)   
 [IDebugThread2::Resume](../vs140/IDebugThread2--Resume.md)