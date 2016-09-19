---
title: "How to: Upgrade Visual C++ Projects to Visual Studio 2015"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9a283ebb-f6d8-49c0-a73e-323979ff56a2
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Upgrade Visual C++ Projects to Visual Studio 2015
When you first open a Visual C++ project that was created in an earlier version of Visual Studio, you might be prompted to update the project. The message asks whether you want to upgrade to the most recent version of the Visual C++ compiler and libraries. The options for upgrading depend on the version of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] that was used to create the project.  
  
 You can use [!INCLUDE[vs_dev12](../vs140/includes/vs_dev12_md.md)] to open, edit, and build [!INCLUDE[win8](../vs140/includes/win8_md.md)] projects that were created in [!INCLUDE[vs_dev11_long](../vs140/includes/vs_dev11_long_md.md)], but to create a new [!INCLUDE[win8](../vs140/includes/win8_md.md)] project, you must use [!INCLUDE[vs_dev11_long](../vs140/includes/vs_dev11_long_md.md)]. (To create a [!INCLUDE[win81](../vs140/includes/win81_md.md)] project, you must use [!INCLUDE[vs_dev12](../vs140/includes/vs_dev12_md.md)].)  
  
 To create a Windows 10 project, you must use [!INCLUDE[vs_dev14](../vs140/includes/vs_dev14_md.md)].  
  
 If you aren't prompted to update the project, you may not have to do anything to upgrade the project.  
  
-   If the project (.vcproj) was created in a version of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] that's older than [!INCLUDE[vs2010](../vs140/includes/vs2010_md.md)], you must update the project.  
  
-   If the project (.vcxproj) was created in [!INCLUDE[vs_dev10_long](../vs140/includes/vs_dev10_long_md.md)],  [!INCLUDE[vs_dev11_long](../vs140/includes/vs_dev11_long_md.md)], or [!INCLUDE[vs_dev12](../vs140/includes/vs_dev12_md.md)] you have two options:  
  
    -   You can skip the update. [!INCLUDE[vs_dev14](../vs140/includes/vs_dev14_md.md)] will load the project without making any changes if it has access to the Visual C++ tools in [!INCLUDE[vs_dev10_long](../vs140/includes/vs_dev10_long_md.md)] with SP1,  [!INCLUDE[vs_dev11_long](../vs140/includes/vs_dev11_long_md.md)], or [!INCLUDE[vs_dev12](../vs140/includes/vs_dev12_md.md)]. You can provide this access by installing the version of Visual Studio that the project was created with on the same machine that has [!INCLUDE[vs_dev14](../vs140/includes/vs_dev14_md.md)]. For more information, see [Installing Visual Studio Versions Side-by-Side](../vs140/Installing-Visual-Studio-Versions-Side-by-Side.md).  
  
    -   You can update the project by allowing [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] to make the changes that are described later in this topic. If you have more than one Visual C++ project in your solution, you must update all of them.  
  
        > [!NOTE]
        >  If you decline the update when you're first prompted, you can update the project later by choosing **Update VC++ project** on the **Project** menu. If the command doesn't appear, then an update isn't required.  
  
## Upgrading a Visual C++ Project  
 If you allow [!INCLUDE[vs_dev14](../vs140/includes/vs_dev14_md.md)] to automatically update the project, these changes are made:  
  
-   Changes the project so that it uses the [!INCLUDE[vs_dev14](../vs140/includes/vs_dev14_md.md)] compiler and libraries (PlatformToolset = VisualStudio v140).  
  
-   For [!INCLUDE[cppcli](../vs140/includes/cppcli_md.md)] projects, changes the TargetFrameworkVersion to the .NET Framework 4.5.2.  
  
## Continuing to Work with a Custom PlatformToolset  
 If you want to continue to work with a custom PlatformToolset in [!INCLUDE[vs_dev14](../vs140/includes/vs_dev14_md.md)], the toolset must be located under %ProgramFiles%\MSBuild\Microsoft.Cpp\v4.0\Platforms\Win32\PlatformToolsets\ on an x86 machine, or under %ProgramFiles (x86)%\MSBuild\Microsoft.Cpp\v4.0\Platforms\Win32\PlatformToolsets\ on an x64 machine. For information about how to create a custom PlatformToolset, see [C++ Native Multi-Targeting](http://go.microsoft.com/fwlink/?LinkId=248587) on the Visual C++ Team blog.  
  
## See Also  
 [Visual C++ Porting and Upgrading Guide](../vs140/Visual-C---Porting-and-Upgrading-Guide.md)   
 [Visual Studio 2015 Compatibility](../vs140/Porting--Migrating--and-Upgrading-Visual-Studio-Projects.md)