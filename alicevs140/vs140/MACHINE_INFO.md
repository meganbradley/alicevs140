---
title: "MACHINE_INFO"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e7564ff2-00b5-4750-8fd5-dc1029a16912
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# MACHINE_INFO
Describes a particular machine.  
  
## Syntax  
  
```cpp#  
typedef struct tagMACHINE_INFO {   
   MACHINE_INFO_FIELDS Fields;  
   BSTR                bstrName;  
   MACHINE_INFO_FLAGS  Flags;  
} MACHINE_INFO;  
```  
  
```c#  
public struct MACHINE_INFO {   
   public uint   Fields;  
   public string bstrName;  
   public uint   Flags;  
};  
```  
  
## Members  
 `Fields`  
 A combination of flags from the [MACHINE_INFO_FIELDS](../vs140/MACHINE_INFO_FIELDS.md) enumeration that specify which fields of the structure are initialized.  
  
 `bstrName`  
 The machine name. Equivalent to calling [GetMachineName](../vs140/IDebugCoreServer2--GetMachineName.md).  
  
 `Flags`  
 A combination of flags from the [MACHINE_INFO_FLAGS](../vs140/MACHINE_INFO_FLAGS.md) enumeration describing the machine attributes.  
  
## Remarks  
 This structure is returned by a call to the [GetMachineInfo](../vs140/IDebugCoreServer2--GetMachineInfo.md) method.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [MACHINE_INFO_FIELDS](../vs140/MACHINE_INFO_FIELDS.md)   
 [GetMachineInfo](../vs140/IDebugCoreServer2--GetMachineInfo.md)