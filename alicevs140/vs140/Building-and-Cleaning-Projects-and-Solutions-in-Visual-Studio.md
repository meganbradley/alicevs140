---
title: "Building and Cleaning Projects and Solutions in Visual Studio"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 710891fd-379e-42c2-a84b-44a7af694ca0
caps.latest.revision: 37
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Building and Cleaning Projects and Solutions in Visual Studio
By using the procedures in this topic, you can build, rebuild, or clean all or some of the projects or project items in a solution. For a step-by-step tutorial, see [Walkthrough: Building an Application](../vs140/Walkthrough--Building-an-Application.md).  
  
> [!NOTE]
>  The UI in your edition of Visual Studio might differ from what this topic describes, depending on your active settings. To change your settings, open the **Tools** menu, and then choose **Import and Export Settings**. For more information, see [Customizing Development Settings in Visual Studio](assetId:///22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### To build, rebuild, or clean an entire solution  
  
1.  In **Solution Explorer**, choose or open the solution.  
  
2.  On the menu bar, choose **Build**, and then choose one of the following commands:  
  
    -   Choose **Build** or **Build Solution** to compile only those project files and components that have changed since the most recent build.  
  
        > [!NOTE]
        >  The **Build** command becomes **Build Solution** when a solution includes more than one project.  
  
    -   Choose **Rebuild Solution** to "clean" the solution and then build all project files and components.  
  
    -   Choose **Clean Solution** to delete any intermediate and output files. With only the project and component files left, new instances of the intermediate and output files can then be built.  
  
### To build or rebuild a single project  
  
1.  In **Solution Explorer**, choose or open the project.  
  
2.  On the menu bar, choose **Build**, and then choose either **Build***ProjectName* or **Rebuild***ProjectName*.  
  
    -   Choose **Build***ProjectName* to build only those project components that have changed since the most recent build.  
  
    -   Choose **Rebuild***ProjectName* to "clean" the project and then build the project files and all project components.  
  
### To build only the startup project and its dependencies  
  
1.  On the menu bar, choose **Tools**, **Options**.  
  
2.  In the **Options** dialog box, expand the **Projects and Solutions** node, and then choose the **Build and Run** page.  
  
     The **Build and Run, Projects and Solutions, Options** dialog box opens.  
  
3.  Select the  **Only build startup projects and dependencies on Run** check box.  
  
     When this check box is selected, only the current startup project and its dependencies are built when you perform either of the following steps:  
  
    -   On the menu bar, choose **Debug**, **Start** (F5).  
  
    -   On the menu bar, choose **Build**, **Build Solution** (CTRL+SHIFT+B).  
  
     When this check box is cleared, all projects, their dependencies, and the solution files are built when you run either of the preceding commands. By default, this check box is cleared.  
  
### To build only the selected Visual C++ project  
  
1.  Choose a [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] project, and then, on the menu bar, choose **Build**, **Project Only**, and one of the following commands:  
  
    -   **Build Only** *ProjectName*  
  
    -   **Rebuild Only** *ProjectName*  
  
    -   **Clean Only** *ProjectName*  
  
    -   **Link Only** *ProjectName*  
  
     These commands apply only to the [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] project that you chose, without building, rebuilding, cleaning, or linking any project dependencies or solution files. Depending on your version of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], the **Project Only** submenu might contain more commands.  
  
### To compile multiple C++ project items  
  
1.  In **Solution Explorer**, choose multiple files that have can be compiled actions, open the shortcut menu for one of those files, and then choose **Compile**.  
  
     If the files have dependencies, the files will be compiled in dependency order. The compile operation will fail if the files require a precompiled header that isn’t available when you compile. The compile operation uses the current active solution configuration.  
  
### To stop a build  
  
1.  Perform either of the following steps:  
  
    -   On the menu bar, choose **Build**, **Cancel**.  
  
    -   Choose the Ctrl + Break keys.  
  
## See Also  
 [How to: Create a Build Log File in Visual Studio](../Topic/How%20to:%20View,%20Save,%20and%20Configure%20Build%20Log%20Files.md)   
 [Overview of Logging in MSBuild](../Topic/Obtaining%20Build%20Logs%20with%20MSBuild.md)   
 [Compiling and Building](../vs140/Compiling-and-Building-in-Visual-Studio.md)   
 [Understanding Build Configurations](../vs140/Understanding-Build-Configurations.md)   
 [Debug and Release Project Configurations](assetId:///0440b300-0614-4511-901a-105b771b236e)   
 [C/C++ Building Reference](../vs140/C-C---Building-Reference.md)   
 [Devenv Command Line Switches](../vs140/Devenv-Command-Line-Switches.md)   
 [Solution and Project Basics](../vs140/Solutions-and-Projects-in-Visual-Studio.md)