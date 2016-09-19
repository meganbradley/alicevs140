---
title: "MSBuild Error MSB4133"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5f18937a-fda1-4315-81f9-7cee02802a6d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB4133
**MSB4133: A default tools version "<x.x.>" was specified, but its definition could not be found.**  
  
 [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] cannot find the Toolset that is defined in the project file as the `DefaultToolsVersion`.  
  
### To correct this error  
  
-   Make sure that `DefaultToolsVersion` is specified correctly, and that this Toolset is defined either in the registry or in the [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] configuration file.  
  
## See Also  
 <xref:Microsoft.Build.BuildEngine.Toolset?qualifyHint=False>   
 [Project Element (MSBuild)](../vs140/Project-Element--MSBuild-.md)   
 [Resources for Troubleshooting MSBuild Errors](../vs140/Additional-MSBuild-Resources.md)