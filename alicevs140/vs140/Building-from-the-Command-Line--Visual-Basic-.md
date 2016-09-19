---
title: "Building from the Command Line (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e61947e9-a42e-4717-a699-5f70a98cdd03
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Building from the Command Line (Visual Basic)
A [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] project is made up of one or more separate source files. During the process known as compilation, these files are brought together into one package—a single executable file that can be run as an application.  
  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] provides a command-line compiler as an alternative to compiling programs from within the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] integrated development environment (IDE). The command-line compiler is designed for situations in which you do not require the full set of features in the IDE—for example, when you are using or writing for computers with limited system memory or storage space.  
  
 When compiling from the command line, you must explicitly reference the Microsoft [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] run-time library through the `/reference` compiler option.  
  
 To compile source files from within the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] IDE, choose the **Build** command from the **Build** menu.  
  
> [!TIP]
>  When you build project files by using the Visual Studio IDE, you can display information about the associated **vbc** command and its switches in the output window. To display this information, open the [Build and Run, Projects and Solutions, Options Dialog Box](../vs140/Options-Dialog-Box---Projects-and-Solutions--Build-and-Run.md), and then set the **MSBuild project build output verbosity** to **Normal** or a higher level of verbosity. For more information, see [How to: View, Save, and Configure Build Log Files](../Topic/How%20to:%20View,%20Save,%20and%20Configure%20Build%20Log%20Files.md).  
  
 You can compile project (.vbproj) files at a command prompt by using MSBuild. For more information, see [MSBuild Command-Line Reference](../vs140/MSBuild-Command-Line-Reference.md) and [Walkthrough: Using MSBuild](../vs140/Walkthrough--Using-MSBuild.md).  
  
## In This Section  
 [How to: Invoke the Command-Line Compiler](../vs140/How-to--Invoke-the-Command-Line-Compiler--Visual-Basic-.md)  
 Describes how to invoke the command-line compiler at the MS-DOS prompt or from a specific subdirectory.  
  
 [Sample Compilation Command Lines](../vs140/Sample-Compilation-Command-Lines--Visual-Basic-.md)  
 Provides a list of sample command lines that you can modify for your own use.  
  
## Related Sections  
 [Visual Basic Command-Line Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)  
 Provides lists of compiler options, organized alphabetically or by purpose.  
  
 [Conditional Compilation](../vs140/Conditional-Compilation-in-Visual-Basic.md)  
 Describes how to compile particular sections of code.  
  
 [Building and Cleaning Projects and Solutions in Visual Studio](../vs140/Building-and-Cleaning-Projects-and-Solutions-in-Visual-Studio.md)  
 Describes how to organize what will be included in different builds, choose project properties, and ensure that projects build in the correct order.