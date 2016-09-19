---
title: "Linker Tools Warning LNK4210"
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
ms.topic: error-reference
ms.assetid: db48cff8-a2be-4a77-8d03-552b42c228fa
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Warning LNK4210
section section exists; there may be unhandled static initializers or terminators  
  
 Some code introduced static initializers or terminators, but the CRT or its equivalent (which needs to run the static initializers or terminators) isn't run when the application starts. Examples of code that would cause this:  
  
-   Global class variable with a constructor, destructor, or virtual function table.  
  
-   Global variable initialized with a non-compile-time constant.  
  
 To fix this problem, try one of the following:  
  
-   Remove all code with static initializers.  
  
-   Do not use [/NOENTRY](../vs140/-NOENTRY--No-Entry-Point-.md).  After you remove /NOENTRY, you may also have to add msvcrt.lib, libcmt.lib, or libcmtd.lib to your linker command line.  
  
-   Add msvcrt.lib, libcmt.lib, or libcmtd.lib to your linker command line.  
  
-   When moving from /clr:pure compilation to /clr, remove the [/ENTRY](../vs140/-ENTRY--Entry-Point-Symbol-.md) option from the linker-line. This will enable CRT initialization allowing static initializers to be executed at application startup.  
  
-   If your project is built with [/ENTRY](../vs140/-ENTRY--Entry-Point-Symbol-.md), and if /ENTRY is passed a function other than `_DllMainCRTStartup`, the function must call CRT_INIT. See [Run-Time Library Behavior](../vs140/Run-Time-Library-Behavior.md) and Knowledge Base article Q94248, [http://support.microsoft.com/default.aspx?scid=kb;en-us;94248](http://support.microsoft.com/default.aspx?scid=kb;en-us;94248) for more information.  
  
 The [/GS](../Topic/-GS%20\(Buffer%20Security%20Check\).md) compiler option requires CRT startup code.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)