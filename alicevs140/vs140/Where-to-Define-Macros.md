---
title: "Where to Define Macros"
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
ms.assetid: 0fc59ec5-5f58-4644-b7da-7b021f7001af
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Where to Define Macros
Define macros in a command line, command file, makefile, or the Tools.ini file.  
  
 In a makefile or the Tools.ini file, each macro definition must appear on a separate line and cannot start with a space or tab. Spaces or tabs around the equal sign are ignored. All [string characters](../vs140/Defining-an-NMAKE-Macro.md) are literal, including surrounding quotation marks and embedded spaces.  
  
 In a command line or command file, spaces and tabs delimit arguments and cannot surround the equal sign. If `string` has embedded spaces or tabs, enclose either the string itself or the entire macro in double quotation marks (" ").  
  
## See Also  
 [Defining an NMAKE Macro](../vs140/Defining-an-NMAKE-Macro.md)