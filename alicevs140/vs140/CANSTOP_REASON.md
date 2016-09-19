---
title: "CANSTOP_REASON"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6da944eb-36cd-4a8c-8d71-544c775cfcc1
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# CANSTOP_REASON
Used to determine if a program can stop execution after reaching a particular point in the execution.  
  
## Syntax  
  
```cpp#  
enum enum_CANSTOP_REASON {   
   CANSTOP_ENTRYPOINT = 0x0000,  
   CANSTOP_STEPIN     = 0x0001  
};  
typedef DWORD CANSTOP_REASON;  
```  
  
```c#  
public enum enum_CANSTOP_REASON {   
   CANSTOP_ENTRYPOINT = 0x0000,  
   CANSTOP_STEPIN     = 0x0001  
};  
```  
  
## Members  
 CANSTOP_ENTRYPOINT  
 Specifies the entry point of the given program.  
  
 CANSTOP_STEPIN  
 Specifies stepping into a function.  
  
## Remarks  
 Passed as an argument to the [GetReason](../vs140/IDebugCanStopEvent2--GetReason.md) method to confirm with the Session Debug Manager (SDM) if it is okay to stop after reaching the entry point of the program or after stepping into a function or method.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [GetReason](../vs140/IDebugCanStopEvent2--GetReason.md)