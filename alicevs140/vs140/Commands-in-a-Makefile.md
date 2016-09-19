---
title: "Commands in a Makefile"
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
ms.assetid: 8085517e-42f4-493b-b8f8-44311fc08c64
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Commands in a Makefile
A description block or inference rule specifies a block of commands to run if the dependency is out-of-date. NMAKE displays each command before running it, unless /S, **.SILENT**, **!CMDSWITCHES**, or @ is used. NMAKE looks for a matching inference rule if a description block is not followed by a commands block.  
  
 A commands block contains one or more commands, each on its own line. No blank line can appear between the dependency or rule and the commands block. However, a line containing only spaces or tabs can appear; this line is interpreted as a null command, and no error occurs. Blank lines are permitted between command lines.  
  
 A command line begins with one or more spaces or tabs. A backslash ( \ ) followed by a newline character is interpreted as a space in the command; use a backslash at the end of a line to continue a command onto the next line. NMAKE interprets the backslash literally if any other character, including a space or tab, follows the backslash.  
  
 A command preceded by a semicolon (;) can appear on a dependency line or inference rule, whether or not a commands block follows:  
  
```  
project.obj : project.c project.h ; cl /c project.c  
```  
  
## What do you want to know more about?  
 [Command modifiers](../vs140/Command-Modifiers.md)  
  
 [Filename-parts syntax](../vs140/Filename-Parts-Syntax.md)  
  
 [Inline files in a makefile](../vs140/Inline-Files-in-a-Makefile.md)  
  
## See Also  
 [NMAKE Reference](../vs140/NMAKE-Reference.md)