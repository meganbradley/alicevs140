---
title: "Expanding Wildcard Arguments"
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
ms.assetid: 80a11c4b-0199-420e-a342-cf1d803be5bc
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expanding Wildcard Arguments
**Microsoft Specific**  
  
 When you run a C program, you can use either of the two wildcards — the question mark (?) and the asterisk (*) — to specify filename and path arguments on the command line.  
  
 By default, wildcards are not expanded in command-line arguments. You can replace the normal argument vector `argv` loading routine with a version that does expand wildcards by linking with the setargv.obj or wsetargv.obj file. If your program uses a `main` function, link with setargv.obj. If your program uses a `wmain` function, link with wsetargv.obj. Both of these have equivalent behavior.  
  
 To link with setargv.obj or wsetargv.obj, use the **/link** option. For example:  
  
 **cl example.c /link setargv.obj**  
  
 The wildcards are expanded in the same manner as operating system commands. (See your operating system user's guide if you are unfamiliar with wildcards.)  
  
 **END Microsoft Specific**  
  
## See Also  
 [Link options](../vs140/Link-Options.md)   
 [The main Function and Program Execution](../vs140/main-Function-and-Program-Execution.md)