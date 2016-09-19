---
title: "Customizing C++ Command-Line Processing"
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
ms.topic: language-reference
ms.assetid: aae01cbb-892b-48b8-8e1f-34f22421f263
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Customizing C++ Command-Line Processing
## Microsoft Specific  
 If your program does not take command-line arguments, you can save a small amount of space by suppressing use of the library routine that performs command-line processing. This routine is called **_setargv** and is described in [Wildcard Expansion](../vs140/Wildcard-Expansion.md). To suppress its use, define a routine that does nothing in the file containing the **main** function, and name it **_setargv**. The call to **_setargv** is then satisfied by your definition of **_setargv**, and the library version is not loaded.  
  
 Similarly, if you never access the environment table through the `envp` argument, you can provide your own empty routine to be used in place of **_setenvp**, the environment-processing routine. Just as with the **_setargv** function, **_setenvp** must be declared as **extern "C"**.  
  
 Your program might make calls to the **spawn** or `exec` family of routines in the C run-time library. If this is the case, you should not suppress the environment-processing routine, since this routine is used to pass an environment from the parent process to the child process.  
  
## END Microsoft Specific  
  
## See Also  
 [main: Program Startup](../vs140/main--Program-Startup.md)