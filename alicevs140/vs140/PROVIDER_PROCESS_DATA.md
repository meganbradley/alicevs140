---
title: "PROVIDER_PROCESS_DATA"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ec2362ed-4a0c-4a09-9d66-8ff04e4f41ee
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# PROVIDER_PROCESS_DATA
This structure provides information about processes running on a machine.  
  
## Syntax  
  
```cpp#  
typedef struct tagPROVIDER_PROCESS_DATA {  
   PROVIDER_FIELDS    Fields;  
   PROGRAM_NODE_ARRAY ProgramNodes;  
   BOOL               fIsDebuggerPresent;  
} PROVIDER_PROCESS_DATA;  
```  
  
```c#  
public struct PROVIDER_PROCESS_DATA {  
   public uint               Fields;  
   public PROGRAM_NODE_ARRAY ProgramNodes;  
   public int                fIsDebuggerPresent;  
}  
```  
  
## Members  
 Fields  
 A combination of flags from the [PROVIDER_FIELDS](../vs140/PROVIDER_FIELDS.md) enumeration, indicating which fields are filled in.  
  
 ProgramNodes  
 A [PROGRAM_NODE_ARRAY](../vs140/PROGRAM_NODE_ARRAY.md) structure that contains an array of program nodes.  
  
 fIsDebuggerPresent  
 Nonzero (`TRUE`) if the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] debugger is running, zero (`FALSE`) if it is not.  
  
## Remarks  
 This structure is passed to the [IDebugProgramProvider2::GetProviderProcessData](../vs140/IDebugProgramProvider2--GetProviderProcessData.md) method where it is filled in.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [PROVIDER_FIELDS](../vs140/PROVIDER_FIELDS.md)   
 [PROGRAM_NODE_ARRAY](../vs140/PROGRAM_NODE_ARRAY.md)   
 [IDebugProgramProvider2::GetProviderProcessData](../vs140/IDebugProgramProvider2--GetProviderProcessData.md)