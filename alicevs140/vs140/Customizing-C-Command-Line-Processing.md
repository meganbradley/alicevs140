---
title: "Customizing C Command-Line Processing"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c20fa11d-b35b-4f3e-93b6-2cd5a1c3c993
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Customizing C Command-Line Processing
If your program does not take command-line arguments, you can save a small amount of space by suppressing use of the library routine that performs command-line processing. This routine is called **_setargv** (or **_wsetargv** in the wide-character environment), as described in [Expanding Wildcard Arguments](../vs140/Expanding-Wildcard-Arguments.md). To suppress its use, define a routine that does nothing in the file containing the **main** function and name it **_setargv** (or **_wsetargv** in the wide-character environment). The call to **_setargv** or **_wsetargv** is then satisfied by your definition of **_setargv** or **_wsetargv** , and the library version is not loaded.  
  
 Similarly, if you never access the environment table through the `envp` argument, you can provide your own empty routine to be used in place of **_setenvp** (or **_wsetenvp**), the environment-processing routine.  
  
 If your program makes calls to the **_spawn** or **_exec** family of routines in the C run-time library, you should not suppress the environment-processing routine, since this routine is used to pass an environment from the spawning process to the new process.  
  
## See Also  
 [The main Function and Program Execution](../vs140/main-Function-and-Program-Execution.md)