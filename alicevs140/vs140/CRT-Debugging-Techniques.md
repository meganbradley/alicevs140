---
title: "CRT Debugging Techniques"
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
ms.assetid: 9be561f6-14a8-44ff-925d-d911d5b8e6ff
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRT Debugging Techniques
If you are debugging a program that uses the C run-time library, these debugging techniques might be useful.  
  
## In This Section  
 [CRT Debug Library Use](../vs140/CRT-Debug-Library-Use.md)  
 Describes the debugging support provided by the C Run-Time Library and provides instructions for accessing the tools.  
  
 [Macros for Reporting](../vs140/Macros-for-Reporting.md)  
 Provides information about the **_RPTn** and **_RPTFn** macros (defined in CRTDBG.H), which replace the use of `printf` statements for debugging.  
  
 [Debug Versions of Heap Allocation Functions](../vs140/Debug-Versions-of-Heap-Allocation-Functions.md)  
 Discusses the special Debug versions of the heap allocation functions, including: how the CRT maps calls, the benefits of calling them explicitly, how to avoid conversion, tracking the separate types of allocations in client blocks, and the results of not defining _DEBUG.  
  
 [CRT Debug Heap Details](../vs140/CRT-Debug-Heap-Details.md)  
 Provides links to memory management and the debug heap, types of blocks on the debug heap, using the debug heap, heap state reporting functions, and tracking heap allocation requests.  
  
 [Debug Hook Function Writing](../vs140/Debug-Hook-Function-Writing.md)  
 Lists links to client block hook functions, allocation hook functions, allocation hooks and CRT memory allocations, and report hook functions.  
  
 [Finding Memory Leaks Using the CRT Library](../vs140/Finding-Memory-Leaks-Using-the-CRT-Library.md)  
 Covers techniques for detecting and isolating memory leaks by using the debugger and the C Run-Time Library.  
  
## Related Sections  
 [Debugging Native Code](../vs140/Debugging-Native-Code.md)  
 Discusses some common debugging problems and techniques for C and C++ applications.  
  
 [Debugger Security](../vs140/Debugger-Security.md)  
 Provides recommendations for more secure debugging.