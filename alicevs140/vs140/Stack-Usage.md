---
title: "Stack Usage"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 383f0072-0438-489f-8829-cca89582408c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Stack Usage
All memory beyond the current address of RSP is considered volatile: The OS, or a debugger, may overwrite this memory during a user debug session, or an interrupt handler. Thus, RSP must always be set before attempting to read or write values to a stack frame.  
  
 This section discusses the allocation of stack space for local variables and the **alloca** intrinsic.  
  
-   [Stack Allocation](../vs140/Stack-Allocation.md)  
  
-   [Dynamic Parameter Stack Area Construction](../vs140/Dynamic-Parameter-Stack-Area-Construction.md)  
  
-   [Function Types](../vs140/Function-Types.md)  
  
-   [malloc Alignment](../vs140/malloc-Alignment.md)  
  
-   [alloca](../vs140/alloca.md)  
  
## See Also  
 [x64 Software Conventions](../vs140/x64-Software-Conventions.md)