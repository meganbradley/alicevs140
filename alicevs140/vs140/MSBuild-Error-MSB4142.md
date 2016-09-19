---
title: "MSBuild Error MSB4142"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 56121c76-f952-43d1-ba23-1d1792fef0bc
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB4142
**MSB4142: MSBuildToolsPath is not the same as MSBuildBinPath for the ToolsVersion "<x.x>".**  
  
 The Toolset definition specifies different values for `MSBuildBinPath` and `MSBuildToolsPath`.  
  
### To correct this error  
  
-   Make sure that the values for `MSBuildBinPath` and `MSBuildToolsPath` are the same in your Toolset definition.  
  
## See Also  
 [Standard and Custom Toolset Configurations](../vs140/Standard-and-Custom-Toolset-Configurations.md)   
 [Project Element (MSBuild)](../vs140/Project-Element--MSBuild-.md)   
 [Resources for Troubleshooting MSBuild Errors](../vs140/Additional-MSBuild-Resources.md)