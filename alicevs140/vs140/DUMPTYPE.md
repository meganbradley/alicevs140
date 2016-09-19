---
title: "DUMPTYPE"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ea8160db-8732-4056-a1d7-892ef72da71e
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# DUMPTYPE
Specifies how much of a program's state (such as running threads, stack frames, and current instruction address) to dump.  
  
## Syntax  
  
```cpp#  
enum enum_DUMPTYPE {   
   DUMP_MINIDUMP = 0,  
   DUMP_FULLDUMP = 1  
};  
typedef DWORD DUMPTYPE;  
```  
  
```c#  
public enum enum_DUMPTYPE {   
   DUMP_MINIDUMP = 0,  
   DUMP_FULLDUMP = 1  
};  
```  
  
## Members  
 DUMP_MINIDUMP  
 Specifies a small, compact dump.  
  
 DUMP_FULLDUMP  
 Specifies a large, complete dump.  
  
## Remarks  
 Passed as an argument to the [WriteDump](../vs140/IDebugProgram2--WriteDump.md) method.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [WriteDump](../vs140/IDebugProgram2--WriteDump.md)