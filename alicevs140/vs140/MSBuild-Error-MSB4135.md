---
title: "MSBuild Error MSB4135"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9192f772-ad13-42f7-b53f-c5e31846fa5f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB4135
**MSB4135: Error reading the toolset information from the registry key "'<key\>'" or a subkey. '<key\>'**  
  
 The custom Toolset information defined in the registry could not be read.  
  
### To correct this error  
  
-   If you have defined a custom Toolset in the registry, make sure that it is in valid registry format, that is has the correct `ToolsVersion` name and that the correct `MSBuildBinPath` or `MSBuildToolsPath` value.  
  
## See Also  
 [Standard and Custom Toolset Configurations](../vs140/Standard-and-Custom-Toolset-Configurations.md)   
 [Project Element (MSBuild)](../vs140/Project-Element--MSBuild-.md)   
 [Resources for Troubleshooting MSBuild Errors](../vs140/Additional-MSBuild-Resources.md)