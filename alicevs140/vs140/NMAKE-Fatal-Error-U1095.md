---
title: "NMAKE Fatal Error U1095"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: a392582b-06db-4568-9c13-450293a4fbda
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NMAKE Fatal Error U1095
expanded command line 'commandline' too long  
  
 After macro expansion, the given command line exceeded the limit on length of command lines for the operating system.  
  
 MS-DOS permits up to 128 characters on a command line.  
  
 If the command is for a program that can accept command-line input from a file, change the command and supply input from either a file on disk or an inline file. For example, LINK and LIB accept input from a response file.