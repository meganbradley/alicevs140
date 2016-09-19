---
title: "Specify Project Settings, Create New Project From Existing Code Files Wizard"
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
ms.assetid: 9b8860c9-d35f-4f18-9565-2934d3d7f569
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Specify Project Settings, Create New Project From Existing Code Files Wizard
Use this page of the Create New Project From Existing Code Files wizard to specify:  
  
-   The build environment for the new project  
  
-   Build settings to match a specific type of new project to generate  
  
## Task List  
 [How to: Create a C++ Project From Existing Code](../vs140/How-to--Create-a-C---Project-from-Existing-Code.md)  
  
## UIElement List  
 **Use Visual Studio**  
 Specifies to use build tools that are included in Visual Studio for building the new project. This option is selected by default.  
  
 **Project Type**  
 Specifies the type of project that the wizard will generate.  
  
 **Windows application project**  
 Indicates that the wizard will generate a project for an executable Windows application. This option is available from the **Project Type** drop-down list box.  
  
 **Console application project**  
 Indicates that the wizard will generate a project for a console application. This option is available from the **Project Type** drop-down list box.  
  
 **Dynamically linked library (DLL) project**  
 Indicates that the wizard will generate a project for an empty dynamic link library application. This option is available from the **Project Type** drop-down list box.  
  
 **Static library (LIB) project**  
 Indicates that the wizard will generate a project for a static library application. This option is available from the **Project Type** drop-down list box.  
  
 **Add support for ATL**  
 Adds ATL support to the new project.  
  
 **Add support for MFC**  
 Adds MFC support to the new project.  
  
 **Add support for the Common Language Runtime**  
 Adds CLR programming support to the new project.  
  
 **Common Language Runtime**  
 Specifies the new project to be compliant with CLR features.  
  
 **Common Language Runtime (old syntax)**  
 Specifies the new project to be compliant with Managed Extensions for C++ syntax, which is CLR programming syntax prior to Visual C++ 2005.  
  
 **Use external build system**  
 Specifies to use build tools that are not included in Visual Studio for building the new project. When this option is selected, you can specify build command lines on the **Specify Debug Configuration Settings** and **Specify Release Configuration Settings** pages.  
  
> [!NOTE]
>  When the **Use External Build System** option is checked, the IDE does not build the new project, so the /D, /I, /FI, /AI, or /FU options are not required for compilation. However, these options must be set correctly in order for IntelliSense to function properly.  
  
## See Also  
 [Specify Debug Configuration Settings, Create New Project From Existing Code Files Wizard](../vs140/Specify-Debug-Configuration-Settings--Create-New-Project-From-Existing-Code-Files-Wizard.md)   
 [Specify Release Configuration Settings, Create New Project From Existing Code Files Wizard](../vs140/Specify-Release-Configuration-Settings--Create-New-Project-From-Existing-Code-Files-Wizard.md)