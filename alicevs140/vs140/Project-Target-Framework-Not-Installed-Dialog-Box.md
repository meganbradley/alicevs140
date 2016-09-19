---
title: "Project Target Framework Not Installed Dialog Box"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 64ce8743-d5bd-447e-ba10-54b2aafe109e
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Project Target Framework Not Installed Dialog Box
You have opened a project which targets a framework that is not installed on your computer. To proceed, you must select one of the options in this dialog box.  
  
> [!NOTE]
>  Whenever you download and install a new framework, you must restart Visual Studio.  
  
## Visual Basic and Visual C#  
 If you opened a Visual Basic or Visual C# project, select one of the following options.  
  
 **Change target to .NET Framework 4.5. You can change back to .NET Framework** *Version*  **at a later time.**  
 Retargets your project to .NET Framework 4.5. You can later reinstall the previous version and then retarget the project.  
  
 **Download the targeting pack for .NET Framework <Version\>. The project will not change.**  
 Opens the Microsoft Download Center website, where you can download the version of the .NET Framework that you want. Your project is unloaded from the solution. After you download and install the desired framework, you must restart Visual Studio, and then reopen the project.  
  
 **Do not load the project.**  
 Leaves the project unloaded from the solution. You can later install the desired Framework and then reload the project.  
  
## Visual C++  
 If you opened a Visual C++ project, select one of the following options.  
  
 **Download the targeting pack for .NET Framework** *Version* **. The project will not change.**  
 Opens the Microsoft Download Center website, where you can download the version of the .NET Framework that you want. After the download finishes, your project is retargeted to that version. Your project is unloaded from the solution. After you download and install the desired framework, you must restart [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], and then reopen the project.  
  
 **Do not load the project.**  
 Leaves the project unloaded from the solution. You can later install the desired Framework and then reload the project.  
  
## See Also  
 [How to: Target a Specific .NET Framework Version](../vs140/How-to--Target-a-Version-of-the-.NET-Framework.md)   
 [Troubleshooting .NET Framework Targeting Errors](../vs140/Troubleshooting-.NET-Framework-Targeting-Errors.md)   
 [Frameworks and References, Common Properties, <Projectname\> Properties Dialog Box](../vs140/Adding-references-in-Visual-C---projects.md)