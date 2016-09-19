---
title: "PROCESS_INFO_FLAGS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 696951ce-701a-40c2-ac8c-b897f3aae6e2
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# PROCESS_INFO_FLAGS
Describes or specifies properties of a process.  
  
## Syntax  
  
```cpp#  
enum enum_PROCESS_INFO_FLAGS {   
   PIFLAG_SYSTEM_PROCESS    = 0x00000001,  
   PIFLAG_DEBUGGER_ATTACHED = 0x00000002,  
   PIFLAG_PROCESS_STOPPED   = 0x00000004,  
   PIFLAG_PROCESS_RUNNING   = 0x00000008,  
};  
typedef DWORD PROCESS_INFO_FLAGS;  
```  
  
```c#  
enum enum_PROCESS_INFO_FLAGS {   
   PIFLAG_SYSTEM_PROCESS    = 0x00000001,  
   PIFLAG_DEBUGGER_ATTACHED = 0x00000002,  
   PIFLAG_PROCESS_STOPPED   = 0x00000004,  
   PIFLAG_PROCESS_RUNNING   = 0x00000008,  
};  
```  
  
## Members  
 PIFLAG_SYSTEM_PROCESS  
 Indicates that the process is a system process.  
  
 PIFLAG_DEBUGGER_ATTACHED  
 Indicates that the process is being debugged by a debugger. It may be a [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] debugger, or it may be some other debugger, for example, WinDbg.  
  
 PIFLAG_PROCESS_STOPPED  
 Indicates the process is stopped. Valid only if `PIFLAG_DEBUGGER_ATTACHED` is also specified. Available in [!INCLUDE[vsprvslong](../vs140/includes/vsprvslong_md.md)] and later.  
  
 PIFLAG_PROCESS_RUNNING  
 Indicates the process is running. Valid only if `PIFLAG_DEBUGGER_ATTACHED` is also specified. Available in [!INCLUDE[vsprvslong](../vs140/includes/vsprvslong_md.md)] and later.  
  
## Remarks  
 Used for the `Flags` member of the [PROCESS_INFO](../vs140/PROCESS_INFO.md) structure.  
  
 These flags may be combined with a bitwise `OR`.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [PROCESS_INFO](../vs140/PROCESS_INFO.md)