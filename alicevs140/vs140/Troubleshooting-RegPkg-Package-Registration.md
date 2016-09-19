---
title: "Troubleshooting RegPkg Package Registration"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f33f822f-697a-4bad-9c10-554b4c8f6246
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Troubleshooting RegPkg Package Registration
> [!NOTE]
>  The preferred way to register packages in Visual Studio is by using .pkgdef files. This allows for extension deployment without having to access the system registry. Pkgdef files are created by using the [CreatePkgDef Utility](../vs140/CreatePkgDef-Utility.md).  
  
 To register a package by using RegPkg in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], you must use the version of RegPkg that is appropriate for your package.  
  
## RegPkg Versions Related to Package Versions  
 There are two versions of RegPkg. One version is included in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. Use this version to register packages that have been built by using one of the following assemblies:  
  
1.  Microsoft.VisualStudioShell.9.0.dll  
  
2.  Microsoft.VisualStudioShell.10.0.dll  
  
3.  Microsoft.VisualStudioShell.11.0.dll  
  
 It cannot register packages that have been built by using the earlier Microsoft.VisualStudio.Shell.dll assembly.  
  
 The earlier version of RegPkg can register packages that have been built by using the Microsoft.VisualStudio.Shell.dll assembly. However, it cannot register packages built by using later versions of that assembly.  
  
## See Also  
 [Releasing a Visual Studio Integration Product](../vs140/Releasing-a-Visual-Studio-Integration-Product.md)