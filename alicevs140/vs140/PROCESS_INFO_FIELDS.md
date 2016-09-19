---
title: "PROCESS_INFO_FIELDS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0d9cc345-3d3a-44d8-ae15-a67acb97a828
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# PROCESS_INFO_FIELDS
Specified what kind of information to retrieve for a process.  
  
## Syntax  
  
```cpp#  
enum enum_PROCESS_INFO_FIELDS {   
   PIF_FILE_NAME             = 0x00000001,  
   PIF_BASE_NAME             = 0x00000002,  
   PIF_TITLE                 = 0x00000004,  
   PIF_PROCESS_ID            = 0x00000008,  
   PIF_SESSION_ID            = 0x00000010,  
   PIF_ATTACHED_SESSION_NAME = 0x00000020,  
   PIF_CREATION_TIME         = 0x00000040,  
   PIF_FLAGS                 = 0x00000080,  
   PIF_ALL                   = 0x000000ff  
};  
typedef DWORD PROCESS_INFO_FIELDS;  
```  
  
```c#  
public enum enum_PROCESS_INFO_FIELDS {   
   PIF_FILE_NAME             = 0x00000001,  
   PIF_BASE_NAME             = 0x00000002,  
   PIF_TITLE                 = 0x00000004,  
   PIF_PROCESS_ID            = 0x00000008,  
   PIF_SESSION_ID            = 0x00000010,  
   PIF_ATTACHED_SESSION_NAME = 0x00000020,  
   PIF_CREATION_TIME         = 0x00000040,  
   PIF_FLAGS                 = 0x00000080,  
   PIF_ALL                   = 0x000000ff  
};  
```  
  
## Members  
 PIF_FILE_NAME  
 Initialize/use the `bstrFileName` field of the [PROCESS_INFO](../vs140/PROCESS_INFO.md) structure.  
  
 PIF_BASE_NAME  
 Initialize/use the `bstrBaseName` field of the `PROCESS_INFO` structure.  
  
 PIF_TITLE  
 Initialize/use the `bstrTitle` field of the `PROCESS_INFO` structure.  
  
 PIF_PROCESS_ID  
 Initialize/use the `ProcessId` field of the `PROCESS_INFO` structure.  
  
 PIF_SESSION_ID  
 Initialize/use the `dwSessionId` field of the `PROCESS_INFO` structure.  
  
 PIF_ATTACHED_SESSION_NAME  
 Initialize/use the `bstrAttachedSessionName` field of the `PROCESS_INFO` structure.  
  
 PIF_CREATION_TIME  
 Initialize/use the `CreationTime` field of the `PROCESS_INFO` structure.  
  
 PIF_FLAGS  
 Initialize/use the `Flags` field of the `PROCESS_INFO` structure.  
  
 PIF_ALL  
 Fills out all fields.  
  
## Remarks  
 Passed to the [GetInfo](../vs140/IDebugProcess2--GetInfo.md) method to indicate which fields of the [PROCESS_INFO](../vs140/PROCESS_INFO.md) structure are to be initialized.  
  
 Also used in `Fields` field of the `PROCESS_INFO` structure to indicate which fields are used and valid.  
  
 These flags may be combined with a bitwise `OR`.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [PROCESS_INFO](../vs140/PROCESS_INFO.md)