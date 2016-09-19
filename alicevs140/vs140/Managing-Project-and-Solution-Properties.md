---
title: "Managing Project and Solution Properties"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d727efc0-1096-4ede-84b6-31a65da22ac0
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Managing Project and Solution Properties
Projects have properties that govern many aspects of compilation, debugging, testing and deploying. Some properties are common among all project types, and some are unique to specific languages or platforms. You access project properties by right-clicking the project node in Solution Explorer and choosing Properties, or by typing properties into the **QuickLaunch** search box in the menu bar.  
  
 ![Project context menu](../vs140/media/vs2015_proj_prop_menu.gif "vs2015_proj_prop_menu")  
  
 .NET projects also have a properties node in the project tree itself.  
  
 ![Properties node in Solution Explorer tree](../vs140/media/VS2015_Props_SE.png "VS2015_Props_SE")  
  
> [!TIP]
>  Solutions have a few properties, and so do project items; these properties are accessed in the [Properties Window](../vs140/Properties-Window.md), not **Project Designer**.  
  
## Project Properties  
 Project Properties are organized into groups and each group has its own property page, and the pages might be different for different languages and project types.  
  
### C# and Visual Basic projects  
 In C# and Visual Basic projects, properties are exposed in the **Project Designer**. The following illustration shows the Build property page for a WPF project in C#:  
  
 ![Visual Studio Project Designer](../vs140/media/VS2015_PropPage_Build.png "VS2015_PropPage_Build")  
  
 For information about each of the property pages in Project Designer, see [Project Properties Reference](../vs140/Project-Properties-Reference.md).  
  
### C++ and JavaScript projects  
 C++ and JavaScript projects have a different user interface for managing project properties. This illustration shows a C++ project property page (JavaScript pages are similar):  
  
 ![Visual C&#43;&#43; project properties](../vs140/media/VS2015_ProjProps_cpp.png "VS2015_ProjProps_cpp")  
  
 For information about C++ project properties, see [Working with Project Properties](../vs140/Working-with-Project-Properties.md). For more information about JavaScript properties, see [Property Pages, JavaScript](../vs140/Property-Pages--JavaScript.md).  
  
## Solution Properties  
 To access properties on the solution, right click the solution node in **Solution Explorer** and choose **Properties**. In the dialog, you can set project configurations for Debug or Release builds, choose which projects(s) should be the startup project when F5 is pressed, and set code analysis options.  
  
## See Also  
 [Solutions and Projects in Visual Studio](../vs140/Solutions-and-Projects-in-Visual-Studio.md)