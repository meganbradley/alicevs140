---
title: "MACHINE_INFO_FIELDS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2d61d206-7d40-4df1-8c88-1b3c9c78821e
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# MACHINE_INFO_FIELDS
Specifies what kind of information to retrieve for a particular machine.  
  
## Syntax  
  
```cpp#  
enum enum_MACHINE_INFO_FIELDS {   
   MCIF_NAME  = 0x00000001,  
   MCIF_FLAGS = 0x00000002,  
   MCIF_ALL   = 0x00000003  
};  
typedef DWORD MACHINE_INFO_FIELDS;  
```  
  
```c#  
public enum enum_MACHINE_INFO_FIELDS {   
   MCIF_NAME  = 0x00000001,  
   MCIF_FLAGS = 0x00000002,  
   MCIF_ALL   = 0x00000003  
};  
```  
  
## Members  
 MCIF_NAME  
 Initialize/use the `bstrName` field in the structure.  
  
 MCIF_FLAGS  
 Initialize/use the `Flags` field in the structure.  
  
 MIF_ALL  
 Initialize/use all of the fields in the structure.  
  
## Remarks  
 These values are passed to the [IDebugCoreServer2::GetMachineInfo](../vs140/IDebugCoreServer2--GetMachineInfo.md) method to indicate which members of the [MACHINE_INFO](../vs140/MACHINE_INFO.md) structure are to be initialized.  
  
 Also used in the `Fields` member of the `MACHINE_INFO` structure to indicate which fields are used and valid.  
  
 These flags may be combined with a bitwise `OR`.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [MACHINE_INFO](../vs140/MACHINE_INFO.md)   
 [IDebugCoreServer2::GetMachineInfo](../vs140/IDebugCoreServer2--GetMachineInfo.md)