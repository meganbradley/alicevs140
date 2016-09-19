---
title: "PROGRAM_NODE_ARRAY"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8eeea600-eda5-4b7c-868a-0b86d177b0a5
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# PROGRAM_NODE_ARRAY
Contains an array of objects that describe programs of interest.  
  
## Syntax  
  
```cpp  
typedef struct tagPROGRAM_NODE_ARRAY {  
   DWORD                dwCount;  
   IDebugProgramNode2** Members;  
} PROGRAM_NODE_ARRAY;  
```  
  
```c#  
public struct tagPROGRAM_NODE_ARRAY {  
   public uint                 dwCount;  
   public IDebugProgramNode2[] Members;  
}  
```  
  
## Members  
 dwCount  
 Number of objects in the `Members` array.  
  
 Members  
 An array of [IDebugProgramNode2](../vs140/IDebugProgramNode2.md) objects describing the programs requested.  
  
## Remarks  
 This structure is part of the [PROVIDER_PROCESS_DATA](../vs140/PROVIDER_PROCESS_DATA.md) structure which in turn is filled in by a call to the [IDebugProgramProvider2::GetProviderProcessData](../vs140/IDebugProgramProvider2--GetProviderProcessData.md) method.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [PROVIDER_PROCESS_DATA](../vs140/PROVIDER_PROCESS_DATA.md)   
 [IDebugProgramNode2](../vs140/IDebugProgramNode2.md)   
 [IDebugProgramProvider2::GetProviderProcessData](../vs140/IDebugProgramProvider2--GetProviderProcessData.md)