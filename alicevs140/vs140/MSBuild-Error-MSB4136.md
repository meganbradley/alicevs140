---
title: "MSBuild Error MSB4136"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6f0543d3-f8c0-44e1-8748-8a71be599bf4
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB4136
**MSB4136: Error reading the configuration information.**  
  
 [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] received an error when it tried to read the Toolset information in the [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] configuration file (msbuild.exe.config).  
  
### To correct this error  
  
-   Make sure that the configuration file is correct and well-formed. For example, if you have customized the .config file by adding a Toolset, check the Toolset definition.  
  
## See Also  
 [Overriding ToolsVersion Settings](../vs140/Overriding-ToolsVersion-Settings.md)   
 [Project Element (MSBuild)](../vs140/Project-Element--MSBuild-.md)   
 [Resources for Troubleshooting MSBuild Errors](../vs140/Additional-MSBuild-Resources.md)