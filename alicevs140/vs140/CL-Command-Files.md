---
title: "CL Command Files"
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
ms.assetid: ec3cea06-2af0-4fe9-a94c-119c9d31b3a9
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CL Command Files
A command file is a text file that contains options and filenames you would otherwise type on the [command line](../vs140/Compiler-Command-Line-Syntax.md) or specify using the [CL environment variable](../vs140/CL-Environment-Variables.md). CL accepts a compiler command file as an argument in the CL environment variable or on the command line. Unlike either the command line or the CL environment variable, a command file allows you to use multiple lines of options and filenames.  
  
 Options and filenames in a command file are processed according to the location of a command filename within the CL environment variable or on the command line. However, if the /link option appears in the command file, all options on the rest of the line are passed to the linker. Options in subsequent lines in the command file and options on the command line after the command file invocation are still accepted as compiler options. For more information on how the order of options affects their interpretation, see [Order of CL Options](../vs140/Order-of-CL-Options.md).  
  
 A command file must not contain the CL command. Each option must begin and end on the same line; you cannot use the backslash (\\) to combine an option across two lines.  
  
 A command file is specified by an at sign (@) followed by a filename; the filename can specify an absolute or relative path.  
  
 For example, if the following command is in a file named RESP:  
  
```  
/Og /link LIBC.LIB  
```  
  
 and you specify the following CL command:  
  
```  
CL /Ob2 @RESP MYAPP.C  
```  
  
 the command to CL is as follows:  
  
```  
CL /Ob2 /Og MYAPP.C /link LIBC.LIB  
```  
  
 Note that the command line and the command-file commands are effectively combined.  
  
## See Also  
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)   
 [Compiler Options](../vs140/Compiler-Options.md)