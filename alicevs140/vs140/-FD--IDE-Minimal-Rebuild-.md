---
title: "-FD (IDE Minimal Rebuild)"
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
H1: /FD (IDE Minimal Rebuild)
ms.assetid: 7ef21b8c-a448-4bb4-9585-a2a870028e17
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -FD (IDE Minimal Rebuild)
**/FD** is not exposed to users except in the [Command Line](../vs140/Command-Line-Property-Pages.md) property page of a C++ project's **Property Pages** dialog box, if and only if [/Gm (Enable Minimal Rebuild)](../vs140/-Gm--Enable-Minimal-Rebuild-.md) is not also selected. **/FD** has no effect other than from the development environment. **/FD** is not exposed in the output of **cl /?**.  
  
 If you do not enable **/Gm** in the development environment, **/FD** will be used. **/FD** ensures that the .idb file has sufficient dependency information. **/FD** is only used by the development environment, and it should not be used from the command line or a build script.  
  
## See Also  
 [Output-File (/F) Options](../vs140/Output-File---F--Options.md)   
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)