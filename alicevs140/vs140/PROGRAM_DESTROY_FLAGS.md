---
title: "PROGRAM_DESTROY_FLAGS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: be00d4a3-d5b8-4159-b632-64577f534883
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# PROGRAM_DESTROY_FLAGS
Enumerates the valid values of the program destroy flags.  
  
## Syntax  
  
```cpp#  
enum enum_PPROGRAM_DESTROY_FLAGS  
{  
   PROGRAM_DESTROY_CONTINUE_DEBUGGING = 0x1  
};  
typedef DWORD PROGRAM_DESTROY_FLAGS;  
```  
  
```c#  
public enum enum_PPROGRAM_DESTROY_FLAGS  
{  
   PROGRAM_DESTROY_CONTINUE_DEBUGGING = 0x1  
};  
```  
  
## Terms  
 PROGRAM_DESTROY_CONTINUE_DEBUGGING  
 Destroy program, but continue to debug.  
  
## Remarks  
 The enumeration is returned by the [IDebugProgramDestroyEventFlags2::GetFlags](../vs140/IDebugProgramDestroyEventFlags2--GetFlags.md) method.  
  
## Requirements  
 Header: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [IDebugProgramDestroyEventFlags2::GetFlags](../vs140/IDebugProgramDestroyEventFlags2--GetFlags.md)