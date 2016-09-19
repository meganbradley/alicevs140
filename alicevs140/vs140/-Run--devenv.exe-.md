---
title: "-Run (devenv.exe)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
H1: /Run (devenv.exe)
ms.assetid: b1f22f9d-39a5-4918-8a2a-4b5c1e872665
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Run (devenv.exe)
Compiles and runs the specified project or solution.  
  
## Syntax  
  
```  
devenv {/run|/r} {SolutionName|ProjectName}  
```  
  
## Arguments  
 `SolutionName`  
 Required. The full path and name of a solution file.  
  
 `ProjectName`  
 Required. The full path and name of a project file.  
  
## Remarks  
 Compiles and runs the specified project or solution according to the settings specified for the active solution configuration. This switch launches the integrated development environment (IDE) and leaves it active after the project or solution has completed running.  
  
-   Enclose strings that include spaces in double quotation marks.  
  
-   Summary information, including errors, can be displayed in the **Command** window, or in any log file specified with the `/out` switch.  
  
## Example  
 This example runs the solution `MySolution` using the active deployment configuration.  
  
```  
devenv /run "C:\Documents and Settings\someuser\My Documents\Visual Studio\Projects\MySolution\MySolution.sln"  
```  
  
## See Also  
 [Devenv Command Line Switches](../vs140/Devenv-Command-Line-Switches.md)   
 [/Runexit (devenv.exe)](../vs140/-Runexit--devenv.exe-.md)   
 [/build](../vs140/-Build--devenv.exe-.md)   
 [/rebuild (Visual Studio)](../vs140/-Rebuild--devenv.exe-.md)   
 [/out (Visual Studio)](../vs140/-Out--devenv.exe-.md)