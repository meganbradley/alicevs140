---
title: "Compiler Command-Line Syntax"
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
ms.assetid: acba2c1c-0803-4a3a-af25-63e849b930a2
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Command-Line Syntax
The CL command line uses the following syntax:  
  
```  
CL [option...] file... [option | file]... [lib...] [@command-file] [/link link-opt...]  
```  
  
 The following table describes input to the CL command.  
  
|Entry|Meaning|  
|-----------|-------------|  
|*option*|One or more [CL options](../vs140/Compiler-Options.md). Note that all options apply to all specified source files. Options are specified by either a forward slash (/) or a dash (–). If an option takes an argument, the option's description documents whether a space is allowed between the option and the arguments. Option names (except for the /HELP option) are case sensitive. See [Order of CL Options](../vs140/Order-of-CL-Options.md) for more information.|  
|`file`|The name of one or more source files, .obj files, or libraries. CL compiles source files and passes the names of the .obj files and libraries to the linker. See [CL Filename Syntax](../vs140/CL-Filename-Syntax.md) for more information.|  
|*lib*|One or more library names. CL passes these names to the linker.|  
|*command-file*|A file that contains multiple options and filenames. See [CL Command Files](../vs140/CL-Command-Files.md) for more information.|  
|*link-opt*|One or more [linker options](../Topic/Linker%20Options.md). CL passes these options to the linker.|  
  
 You can specify any number of options, filenames, and library names, as long as the number of characters on the command line does not exceed 1024, the limit dictated by the operating system.  
  
 For information about the return value of cl.exe, see [Return Value of cl.exe](../vs140/Return-Value-of-cl.exe.md) .  
  
> [!NOTE]
>  The command-line input limit of 1024 characters is not guaranteed to remain the same in future releases of Windows.  
  
## See Also  
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)   
 [Compiler Options](../vs140/Compiler-Options.md)