---
title: "PROVIDER_FIELDS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 39631545-2b0e-45b4-978b-d63656484b02
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# PROVIDER_FIELDS
Specifies properties associated with a program provider.  
  
## Syntax  
  
```cpp#  
enum enum_PROVIDER_FIELDS {  
   PFIELD_PROGRAM_NODES       = 0x01,  
   PFIELD_IS_DEBUGGER_PRESENT = 0x02  
};  
typedef DWORD PROVIDER_FIELDS;  
```  
  
```c#  
public enum enum_PROVIDER_FIELDS {  
   PFIELD_PROGRAM_NODES       = 0x01,  
   PFIELD_IS_DEBUGGER_PRESENT = 0x02  
};  
```  
  
## Members  
 PFIELD_PROGRAM_NODES  
 The `ProgramNodes` field is valid.  
  
 PFIELD_IS_DEBUGGER_PRESENT  
 The `fIsDebuggerPresent` field is valid.  
  
## Remarks  
 These values are returned in the `Fields` member of the [PROVIDER_PROCESS_DATA](../vs140/PROVIDER_PROCESS_DATA.md) structure to indicate which fields of the structure were explicitly filled in.  
  
 These values can be combined with a bitwise `OR`.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [PROVIDER_PROCESS_DATA](../vs140/PROVIDER_PROCESS_DATA.md)