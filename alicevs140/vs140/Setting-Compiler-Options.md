---
title: "Setting Compiler Options"
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
ms.assetid: 4b079f5b-0017-4124-aad6-0d2b58e427e0
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Setting Compiler Options
C and C++ compiler options can be set either in the development environment or on the command line.  
  
## In the Development Environment  
 You can set compiler options for each project in its **Property Pages** dialog box. In the left pane, select **Configuration Properties**, **C/C++** and then choose the compiler option category. The topic for each compiler option describes how it can be set and where it is found in the development environment. See [Compiler Options](../vs140/Compiler-Options.md) for a complete list.  
  
## Outside the Development Environment  
 You can set compiler (CL.exe) options:  
  
-   [On the command line](../vs140/Compiler-Command-Line-Syntax.md)  
  
-   [In command files](../vs140/CL-Command-Files.md)  
  
-   [In the CL environment variable](../vs140/CL-Environment-Variables.md)  
  
 Options specified in the CL environment variable are used every time you invoke CL. If a command file is named in the CL environment variable or on the command line, the options specified in the command file are used. Unlike either the command line or the CL environment variable, a command file allows you to use multiple lines of options and filenames.  
  
 Compiler options are processed "left to right," and when a conflict is detected, the last (rightmost) option wins. The CL environment variable is processed before the command line, so in any conflicts between CL and the command line, the command line takes precedence.  
  
## Additional Compiler Topics  
  
-   [Fast Compilation](../vs140/Fast-Compilation.md)  
  
-   [CL Invokes the Linker](../vs140/CL-Invokes-the-Linker.md)  
  
## See Also  
 [C/C++ Building Reference](../vs140/C-C---Building-Reference.md)   
 [Compiler Options](../vs140/Compiler-Options.md)