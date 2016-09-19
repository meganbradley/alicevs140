---
title: "AD_PROCESS_ID"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4cb40d12-2e92-4f09-83f4-689928bd65b3
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# AD_PROCESS_ID
Specifies the process ID, which may be either a system ID or a GUID.  
  
## Syntax  
  
```cpp#  
typedef struct _AD_PROCESS_ID {  
   AD_PROCESS_ID_TYPE ProcessIdType;  
   union {  
      DWORD dwProcessId;   
      GUID  guidProcessId;   
      DWORD dwUnused;   
   } ProcessId;  
} AD_PROCESS_ID;  
```  
  
```c#  
public struct AD_PROCESS_ID {  
   AD_PROCESS_ID_TYPE ProcessIdType;  
   DWORD              dwProcessId;   
   GUID               guidProcessId;   
   DWORD              dwUnused;   
};  
```  
  
## Members  
 `ProcessIdType`  
 A value from the [AD_PROCESS_ID_TYPE](../vs140/AD_PROCESS_ID_TYPE.md) enumeration specifying how to interpret the `ProcessId` union (or, for managed code, which member of the structure to access).  
  
 dwProcessId  
 The process ID as a value from the system.  
  
 guidProcessId  
 The process ID as a GUID.  
  
 dwUnused  
 Padding.  
  
## Remarks  
 This structure is passed to the following methods:  
  
-   [IDebugProgramProvider2::GetProviderProgramNode](../vs140/IDebugProgramProvider2--GetProviderProgramNode.md)  
  
-   [IDebugProgramProvider2::WatchForProviderEvents](../vs140/IDebugProgramProvider2--WatchForProviderEvents.md)  
  
-   [IDebugProgramProvider2::GetProviderProcessData](../vs140/IDebugProgramProvider2--GetProviderProcessData.md)  
  
-   [IDebugPort2::GetProcess](../vs140/IDebugPort2--GetProcess.md)  
  
 And is returned from the following methods:  
  
-   [IDebugProcess2::GetPhysicalProcessId](../vs140/IDebugProcess2--GetPhysicalProcessId.md)  
  
-   [IDebugProgramHost2::GetHostId](../vs140/IDebugProgramHost2--GetHostId.md)  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [GetProcess](../vs140/IDebugPort2--GetProcess.md)   
 [PROCESS_INFO](../vs140/PROCESS_INFO.md)   
 [AD_PROCESS_ID_TYPE](../vs140/AD_PROCESS_ID_TYPE.md)   
 [GetPhysicalProcessId](../vs140/IDebugProcess2--GetPhysicalProcessId.md)   
 [GetHostId](../vs140/IDebugProgramHost2--GetHostId.md)   
 [IDebugProgramProvider2::GetProviderProgramNode](../vs140/IDebugProgramProvider2--GetProviderProgramNode.md)   
 [IDebugProgramProvider2::WatchForProviderEvents](../vs140/IDebugProgramProvider2--WatchForProviderEvents.md)   
 [IDebugProgramProvider2::GetProviderProcessData](../vs140/IDebugProgramProvider2--GetProviderProcessData.md)