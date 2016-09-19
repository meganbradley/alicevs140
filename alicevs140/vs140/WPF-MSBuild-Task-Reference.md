---
title: "WPF MSBuild Task Reference"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
  - jsharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 96df0370-e50f-4ffc-9771-b12fb8721143
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WPF MSBuild Task Reference
The Windows Presentation Foundation (WPF) build process extends Microsoft build engine (MSBuild) with an additional set of build tasks, including tasks to compile markup and process resources.  
  
## In This Section  
 [FileClassifier Task](../Topic/FileClassifier%20Task.md)  
 Classifies a set of source resources as those that will be embedded into an assembly. If a resource is not localizable, it is embedded into the main application assembly; otherwise, it is embedded into a satellite assembly.  
  
 [GenerateTemporaryTargetAssembly Task](../Topic/GenerateTemporaryTargetAssembly%20Task.md)  
 Generates an assembly if at least one [!INCLUDE[TLA#tla_xaml](../vs140/includes/TLA#tla_xaml_md.md)] page in a project references a type that is declared locally in that project. The generated assembly is removed after the build process is completed, or if the build process fails.  
  
 [GetWinFXPath Task](../vs140/GetWinFXPath-Task.md)  
 Returns the directory of the current [!INCLUDE[TLA#tla_winfx](../vs140/includes/TLA#tla_winfx_md.md)] runtime.  
  
 [MarkupCompilePass1 Task](../Topic/MarkupCompilePass1%20Task.md)  
 Converts non-localizable [!INCLUDE[TLA#tla_xaml](../vs140/includes/TLA#tla_xaml_md.md)] project files to compiled binary format.  
  
 [MarkupCompilePass2 Task](../Topic/MarkupCompilePass2%20Task.md)  
 Performs second-pass markup compilation on [!INCLUDE[TLA#tla_xaml](../vs140/includes/TLA#tla_xaml_md.md)] files that reference types in the same project.  
  
 [MergeLocalizationDirectives Task](../vs140/MergeLocalizationDirectives-Task.md)  
 Merges the localization attributes and comments of one or more [!INCLUDE[TLA2#tla_xaml](../vs140/includes/TLA2#tla_xaml_md.md)] binary format files into a single file for the whole assembly.  
  
 [ResourcesGenerator Task](../vs140/ResourcesGenerator-Task.md)  
 Embeds one or more resources (.jpg, .ico, .bmp, [!INCLUDE[TLA2#tla_xaml](../vs140/includes/TLA2#tla_xaml_md.md)] in binary format, and other extension types) into a .resources file.  
  
 [UidManager Task](../vs140/UidManager-Task.md)  
 Checks, updates, or removes unique identifiers (UIDs), in order to localize all [!INCLUDE[TLA#tla_xaml](../vs140/includes/TLA#tla_xaml_md.md)] elements that are included in the source [!INCLUDE[TLA2#tla_xaml](../vs140/includes/TLA2#tla_xaml_md.md)] files.  
  
 [UpdateManifestForBrowserApplication Task](../vs140/UpdateManifestForBrowserApplication-Task.md)  
 Adds the **<hostInBrowser /\>** element to the application manifest (*projectname*.exe.manifest) when a [!INCLUDE[TLA#tla_xbap](../vs140/includes/TLA#tla_xbap_md.md)] project is built.  
  
## See Also  
 [MSBuild](assetId:///7c49aba1-ee6c-47d8-9de1-6f29a906e20b)