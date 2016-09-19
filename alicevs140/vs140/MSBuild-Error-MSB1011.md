---
title: "MSBuild Error MSB1011"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f3cb16e5-288c-4dba-941f-a0ed3bf92db7
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB1011
**Specify which project or solution file to use because this folder contains more than one project or solution file.**  
  
 If a project file is not specified at the command line, [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] searches the current working directory for a file that has a file extension that ends in "proj" or "sln" and uses that file. The current working directory contains more than one file that has a file extension that ends in "proj" or "sln".  
  
### To correct this error  
  
1.  Include the project file name on the command line. For example, instead of typing `msbuild`, type `msbuild myapp.proj`.  
  
## See Also  
 [MSBuild Command Line Reference](../vs140/MSBuild-Command-Line-Reference.md)