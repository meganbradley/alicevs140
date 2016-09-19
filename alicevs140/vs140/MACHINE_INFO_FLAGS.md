---
title: "MACHINE_INFO_FLAGS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1482095d-9a2e-4ef1-9e14-362c0b85194e
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# MACHINE_INFO_FLAGS
Used to describe a machine.  
  
## Syntax  
  
```cpp#  
enum enum_MACHINE_INFO_FLAGS {   
   MCIFLAG_TERMINAL_SERVICES_AVAILABLE = 0x00000001  
};  
typedef DWORD MACHINE_INFO_FLAGS;  
```  
  
```c#  
public enum enum_MACHINE_INFO_FLAGS {   
   MCIFLAG_TERMINAL_SERVICES_AVAILABLE = 0x00000001  
};  
```  
  
## Members  
 MCIFLAG_TERMINAL_SERVICES_AVAILABLE  
 Indicates that terminal services are available.  
  
## Remarks  
 Used as the `Flags` member of the [MACHINE_INFO](../vs140/MACHINE_INFO.md) structure.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [MACHINE_INFO_FIELDS](../vs140/MACHINE_INFO_FIELDS.md)