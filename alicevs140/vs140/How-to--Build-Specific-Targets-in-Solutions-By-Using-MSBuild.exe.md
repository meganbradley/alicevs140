---
title: "How to: Build Specific Targets in Solutions By Using MSBuild.exe"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f46feb9b-4c16-4fec-b6e1-36a959692ba3
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Build Specific Targets in Solutions By Using MSBuild.exe
You can use MSBuild.exe to build specific targets of specific projects in a solution.  
  
### To build a specific target of a specific project in a solution  
  
1.  At the command line, type `MSBuild.exe <SolutionName>.sln`, where `<SolutionName>` corresponds to the file name of the solution that contains the target that you want to execute.  
  
2.  Specify the target after the **/t** switch in the format *ProjectName*:*TargetName*.  
  
## Example  
 The following example executes the `Rebuild` target of the `NotInSlnFolder` project, and then executes the `Clean` target of the `InSolutionFolder` project, which is located in the `NewFolder` solution folder.  
  
```  
msbuild SlnFolders.sln /t:NotInSlnfolder:Rebuild;NewFolder\InSolutionFolder:Clean  
```  
  
## See Also  
 [MSBuild Command Line Reference](../vs140/MSBuild-Command-Line-Reference.md)   
 [MSBuild Reference](../Topic/MSBuild%20Reference.md)   
 [MSBuild](../Topic/MSBuild.md)   
 [MSBuild Concepts](../vs140/MSBuild-Concepts.md)