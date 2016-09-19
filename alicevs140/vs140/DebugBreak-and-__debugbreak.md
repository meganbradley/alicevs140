---
title: "DebugBreak and __debugbreak"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9787c795-df94-4f48-bc8d-3bf899b67421
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DebugBreak and __debugbreak
You can call the DebugBreak Win32 function or the [__debugbreak](../vs140/__debugbreak.md) intrinsic at any point in your code. `DebugBreak` and `__debugbreak` have the same effect as setting a breakpoint at that location.  
  
 Because `DebugBreak` is a call to a system function, system debug symbols must be installed to ensure the correct call stack information is displayed after breaking. Otherwise, the call stack information displayed by the debugger may be off by one frame. If you use `__debugbreak`, symbols are not required.  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)   
 [Debugger Security](../vs140/Debugger-Security.md)   
 [Debugging Native Code](../vs140/Debugging-Native-Code.md)   
 [Specify Symbol (.pdb) and Source Files in the Visual Studio Debugger](../vs140/Specify-Symbol--.pdb--and-Source-Files-in-the-Visual-Studio-Debugger.md)