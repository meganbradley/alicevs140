---
title: "-Clean (devenv.exe)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
H1: /Clean (devenv.exe)
ms.assetid: 79929dfd-22c9-4cec-a0d0-a16f15b8f7e4
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Clean (devenv.exe)
Cleans all intermediary files and output directories.  
  
## Syntax  
  
```  
devenv FileName /Clean [ /project projectnameorfile [/projectconfig name ] ]  
```  
  
## Arguments  
 `FileName`  
 Required. The full path and name of the solution file or project file.  
  
 /project `ProjName`  
 Optional. The path and name of a project file within the solution. You can enter a relative path from the `SolutionName` folder to the project file, or the project's display name, or the full path and name of the project file.  
  
 /projectconfig `ProjConfigName`  
 Optional. The name of a project build configuration to be used when cleaning the `/project` named.  
  
## Remarks  
 This switch performs the same function as the **Clean Solution** menu command within the integrated development environment (IDE).  
  
 Enclose strings that include spaces in double quotation marks.  
  
 Summary information for cleans and builds, including errors, can be displayed in the **Command** window, or in any log file specified with the `/out` switch.  
  
## Example  
 The first example cleans the `MySolution` solution, using the default configuration specified in the solution file.  
  
 The second example cleans the project `CSharpConsoleApp`, using the `Debug` project build configuration within the `Debug` solution configuration of `MySolution`.  
  
```  
Devenv "C:\Documents and Settings\someuser\My Documents\Visual Studio\Projects\MySolution\MySolution.sln" /Clean  
  
devenv "C:\Documents and Settings\someuser\My Documents\Visual Studio\Projects\MySolution\MySolution.sln" /Clean /project "CSharpWinApp\CSharpWinApp.csproj" /projectconfig "Debug"   
```  
  
## See Also  
 [Devenv Command Line Switches](../vs140/Devenv-Command-Line-Switches.md)   
 [/Build (devenv.exe)](../vs140/-Build--devenv.exe-.md)   
 [/Rebuild (devenv.exe)](../vs140/-Rebuild--devenv.exe-.md)   
 [/out (Visual Studio)](../vs140/-Out--devenv.exe-.md)