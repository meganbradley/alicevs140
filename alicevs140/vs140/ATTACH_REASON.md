---
title: "ATTACH_REASON"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 159fb70b-a344-4ba6-9115-b7eaa16e228f
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# ATTACH_REASON
Specifies the reason for the debug engine (DE) to attach to a program node.  
  
## Syntax  
  
```cpp#  
enum enum_ATTACH_REASON {   
   ATTACH_REASON_LAUNCH = 0x0001,  
   ATTACH_REASON_USER   = 0x0002,  
   ATTACH_REASON_AUTO   = 0x0003  
};  
typedef DWORD ATTACH_REASON;  
```  
  
```c#  
public enum enum_ATTACH_REASON {   
   ATTACH_REASON_LAUNCH = 0x0001,  
   ATTACH_REASON_USER   = 0x0002,  
   ATTACH_REASON_AUTO   = 0x0003  
};  
```  
  
## Members  
 ATTACH_REASON_AUTO  
 Attach because the process is currently in debug mode.  
  
 ATTACH_REASON_LAUNCH  
 Attach because the process has been launched.  
  
 ATTACH_REASON_USER  
 Attach because of a user request.  
  
## Remarks  
 These values are used as a parameter to the [Attach](../vs140/IDebugEngine2--Attach.md) and [IDebugProgramEx2::Attach](../vs140/IDebugProgramEx2--Attach.md) methods.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [Attach](../vs140/IDebugEngine2--Attach.md)   
 [IDebugProgramEx2::Attach](../vs140/IDebugProgramEx2--Attach.md)