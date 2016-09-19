---
title: "IDebugProgram2::Attach"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: de069fbf-a565-4905-b102-f5658c55aacd
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgram2::Attach
Attaches to the program.  
  
## Syntax  
  
```cpp#  
HRESULT Attach(   
   IDebugEventCallback2* pCallback  
);  
```  
  
```c#  
int Attach(   
   IDebugEventCallback2 pCallback  
);  
```  
  
#### Parameters  
 `pCallback`  
 [in] An [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) object to be used for debug event notification.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. The following table shows some possible error codes.  
  
|Value|Description|  
|-----------|-----------------|  
|`E_ATTACH_DEBUGGER_ALREADY_ATTACHED`|The specified program is already attached to the debugger.|  
|`E_ATTACH_DEBUGGEE_PROCESS_SECURITY_VIOLATION`|A security violation occurred during the attach procedure.|  
|`E_ATTACH_CANNOT_ATTACH_TO_DESKTOP`|A desktop program cannot be attached to the debugger.|  
  
## Remarks  
 A debug engine (DE) never calls this method to attach to a program. If the DE runs in the program's address space, the [IDebugProgramNodeAttach2::OnAttach](../vs140/IDebugProgramNodeAttach2--OnAttach.md) method is called. If the DE runs in the session debug manager's (SDM) address space, the [Attach](../vs140/IDebugEngine2--Attach.md) method is called.  
  
## See Also  
 [IDebugProgram2](../vs140/IDebugProgram2.md)   
 [IDebugEventCallback2](../Topic/IDebugEventCallback2.md)   
 [IDebugProgramNodeAttach2::OnAttach](../vs140/IDebugProgramNodeAttach2--OnAttach.md)   
 [Attach](../vs140/IDebugEngine2--Attach.md)