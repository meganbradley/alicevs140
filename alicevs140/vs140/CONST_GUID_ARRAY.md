---
title: "CONST_GUID_ARRAY"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bd55e7d8-372c-4c3e-9eed-28f6b415a5db
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# CONST_GUID_ARRAY
A structure that holds a list of `GUID`s.  
  
## Syntax  
  
```cpp#  
typedef struct tagCONST_GUID_ARRAY {  
   DWORD       dwCount;  
   CONST GUID* Members;  
} CONST_GUID_ARRAY;  
```  
  
```c#  
public struct CONST_GUID_ARRAY {  
   public uint   dwCount;  
   public Guid[] Members;  
}  
```  
  
## Members  
 dwCount  
 Number of `GUID`s in the `Members` array.  
  
 Members  
 Array of `GUID`s.  
  
## Remarks  
 This structure is passed to the [IDebugProgramPublisher2::PublishProgram](../vs140/IDebugProgramPublisher2--PublishProgram.md) method, and is returned from the [IDebugProgramProvider2::GetProviderProcessData](../vs140/IDebugProgramProvider2--GetProviderProcessData.md) and [IDebugProgramProvider2::WatchForProviderEvents](../vs140/IDebugProgramProvider2--WatchForProviderEvents.md) methods.  
  
 The owner of an instance of this structure is responsible for freeing any memory allocated.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [IDebugProgramPublisher2::PublishProgram](../vs140/IDebugProgramPublisher2--PublishProgram.md)   
 [IDebugProgramProvider2::GetProviderProcessData](../vs140/IDebugProgramProvider2--GetProviderProcessData.md)   
 [IDebugProgramProvider2::WatchForProviderEvents](../vs140/IDebugProgramProvider2--WatchForProviderEvents.md)