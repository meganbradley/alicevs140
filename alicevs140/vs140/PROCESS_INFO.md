---
title: "PROCESS_INFO"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 260c33cc-a05e-4645-84b6-536d0b3b0537
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# PROCESS_INFO
Contains information about a process.  
  
## Syntax  
  
```cpp#  
typedef struct tagPROCESS_INFO {   
   PROCESS_INFO_FIELDS Fields;  
   BSTR                bstrFileName;  
   BSTR                bstrBaseName;  
   BSTR                bstrTitle;  
   AD_PROCESS_ID       ProcessId;  
   DWORD               dwSessionId;  
   BSTR                bstrAttachedSessionName;  
   FILETIME            CreationTime;  
   PROCESS_INFO_FLAGS  Flags;  
} PROCESS_INFO;  
```  
  
```c#  
public struct PROCESS_INFO {   
   public uint          Fields;  
   public string        bstrFileName;  
   public string        bstrBaseName;  
   public string        bstrTitle;  
   public AD_PROCESS_ID ProcessId;  
   public uint          dwSessionId;  
   public string        bstrAttachedSessionName;  
   public FILETIME      CreationTime;  
   public uint          Flags;  
};  
```  
  
## Members  
 Fields  
 A combination of flags from the [PROCESS_INFO_FIELDS](../vs140/PROCESS_INFO_FIELDS.md) enumeration that specify which fields are filled out.  
  
 bstrFileName  
 The full path name of the process. Equivalent to calling the [IDebugProcess2::GetName](../vs140/IDebugProcess2--GetName.md) method with the parameter `GN_FILENAME`.  
  
 bstrBaseName  
 The file name and extension of the process. Equivalent to calling the `IDebugProcess2::Getname` method with the parameter `GN_BASENAME`.  
  
 bstrTitle  
 The title of the process, if one exists. Equivalent to calling the `IDebugProcess2::Getname` method with the parameter `GN_TITLE`.  
  
 ProcessId  
 The [AD_PROCESS_ID](../vs140/AD_PROCESS_ID.md) structure that identifies the process. Equivalent to calling the [IDebugProcess2::GetPhysicalProcessId](../vs140/IDebugProcess2--GetPhysicalProcessId.md) method.  
  
 dwSessionId  
 The identifier of the debug session that this process is running in.  
  
 bstrAttachedSessionName  
 The attached session name. Equivalent to calling the [IDebugProcess2::GetAttachedSessionName](../vs140/IDebugProcess2--GetAttachedSessionName.md) method.  
  
 CreationTime  
 The time the process was created.  
  
 Flags  
 A combination of flags from the [PROCESS_INFO_FLAGS](../vs140/PROCESS_INFO_FLAGS.md) enumeration that specify properties of the process.  
  
## Remarks  
 This structure is passed to the [GetInfo](../vs140/IDebugProcess2--GetInfo.md) method where it is filled in.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [PROCESS_INFO_FIELDS](../vs140/PROCESS_INFO_FIELDS.md)   
 [PROCESS_INFO_FLAGS](../vs140/PROCESS_INFO_FLAGS.md)   
 [GetInfo](../vs140/IDebugProcess2--GetInfo.md)   
 [IDebugProcess2::GetName](../vs140/IDebugProcess2--GetName.md)   
 [IDebugProcess2::GetPhysicalProcessId](../vs140/IDebugProcess2--GetPhysicalProcessId.md)   
 [IDebugProcess2::GetAttachedSessionName](../vs140/IDebugProcess2--GetAttachedSessionName.md)