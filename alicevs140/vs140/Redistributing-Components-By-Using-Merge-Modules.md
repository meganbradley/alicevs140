---
title: "Redistributing Components By Using Merge Modules"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 93b84211-bf9b-4a78-9f22-474ac2ef7840
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Redistributing Components By Using Merge Modules
[!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] includes [merge modules](http://msdn.microsoft.com/library/aa367434) for each [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] component that's licensed to be redistributed with an application. When a merge module is compiled in a Windows Installer setup file, it enables the deployment of specific DLLs to computers that have a specific platform. In your setup file, specify that the merge modules are prerequisites for your application. When [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] is installed, the merge modules are installed in \Program Files\Common Files\Merge Modules\\. (Only non-debug versions of [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] DLLs may be redistributed.) For more information and a link to a list of merge modules that are licensed for redistribution, see [Redistributing Visual C++ Files](../vs140/Redistributing-Visual-C---Files.md).  
  
 You can use merge modules to enable the installation of redistributable [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] DLLs into the %SYSTEMROOT%\system32\ folder. ([!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] itself uses this technique.) However, installation to this folder will fail unless the installing user has administrator rights.  
  
 We recommend that you not use merge modules except when you don't have to service your application and you don't have dependencies on more than one version of the DLLs. Merge modules for different versions of the same DLL cannot be included in one installer, and merge modules make it difficult to service DLLs independently of your application. Instead, we recommend that you install a [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] Redistributable Package.  
  
## See Also  
 [Redistributing Visual C++ Files](../vs140/Redistributing-Visual-C---Files.md)