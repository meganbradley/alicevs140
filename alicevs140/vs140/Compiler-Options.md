---
title: "Compiler Options"
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
ms.assetid: ed3376c8-bef4-4c9a-80e9-3b5da232644c
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Options
cl.exe is a tool that controls the Microsoft C and C++ compilers and linker. cl.exe can be run only on operating systems that support Microsoft Visual Studio.  
  
> [!NOTE]
>  You can start this tool only from the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] command prompt. You cannot start it from a system command prompt or from File Explorer.  
  
 The compilers produce Common Object File Format (COFF) object (.obj) files. The linker produces executable (.exe) files or dynamic-link libraries (DLLs).  
  
 Note that all compiler options are case sensitive.  
  
 To compile without linking, use [/c](../Topic/-c%20\(Compile%20Without%20Linking\).md).  
  
## Finding an Option  
 To find a particular compiler option, see one of the following lists:  
  
-   [Compiler Options Listed Alphabetically](../vs140/Compiler-Options-Listed-Alphabetically.md)  
  
-   [Compiler Options Listed by Category](../vs140/Compiler-Options-Listed-by-Category.md)  
  
## Specifying Options  
 The topic for each compiler option discusses how it can be set in the development environment. For information on specifying options outside the development environment, see:  
  
-   [Compiler Command-Line Syntax](../vs140/Compiler-Command-Line-Syntax.md)  
  
-   [CL Command Files](../vs140/CL-Command-Files.md)  
  
-   [CL Environment Variables](../vs140/CL-Environment-Variables.md)  
  
## Related Build Tools  
 Use [NMAKE](../vs140/NMAKE-Reference.md) to build your output file.  
  
 Use [BSCMAKE](../vs140/BSCMAKE-Reference.md) to support class browsing.  
  
 [Linker options](../Topic/Linker%20Options.md) also affect how your program is built.  
  
## See Also  
 [C/C++ Building Reference](../vs140/C-C---Building-Reference.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)   
 [Fast Compilation](../vs140/Fast-Compilation.md)   
 [CL Invokes the Linker](../vs140/CL-Invokes-the-Linker.md)