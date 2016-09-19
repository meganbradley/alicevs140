---
title: "Solution Configuration"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f22cfc75-3e31-4e0d-88a9-3ca99539203b
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Solution Configuration
Solution configurations store solution-level properties. They direct the behavior of the **Start** (F5) key and **Build** commands. By default, these commands build and start the debug configuration. Both commands execute in the context of a solution configuration. This means that the user can expect F5 to start and build whatever the active solution is configured through the settings. The environment is designed to optimize for solutions rather than projects when it comes to building and running.  
  
 The standard Visual Studio toolbar contains a Start button and a solution configuration drop-down to the right of the Start button. This list allows users to choose the configuration to be started when F5 is pressed, create their own solution configurations, or edit an existing configuration.  
  
> [!NOTE]
>  There are no extensibility interfaces to create or edit the solution configurations. You must use `DTE.SolutionBuilder`. However, there are extensibility APIs for managing the solution build. For more information, see <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionBuildManager2?qualifyHint=False>.  
  
 Here is how you can implement the solution configurations supported by your project type:  
  
-   Project  
  
     Displays the names of projects found in the current solution.  
  
-   Configuration  
  
     To provide the list of configurations supported by your project type and displayed in the property pages, implement <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider2?qualifyHint=False>.  
  
     The Configuration column displays the name of the project configuration to build in this solution configuration, and lists all of the project configurations when you click the arrow button. The environment calls the <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider2.GetCfgNames?qualifyHint=False> method to fill out this list. If the <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider2.GetCfgProviderProperty?qualifyHint=False> method indicates that the project supports configuration editing, New or Edit selections are also displayed under the Configuration heading. Each of these selections launch dialog boxes that call methods of the `IVsCfgProvider2` interface to edit the project's configurations.  
  
     If a project does not support configurations, the Configuration column displays None and is disabled.  
  
-   Platform  
  
     Displays the platform the selected project configuration builds for, and lists all of the available platforms for the project when you click the arrow button. The environment calls the <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider2.GetPlatformNames?qualifyHint=False> method to fill out this list. If the <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider2.GetCfgProviderProperty?qualifyHint=False> method indicates that the project supports platform editing, New or Edit selections are also displayed under the Platform heading. Each of these selections launch dialog boxes that call `IVsCfgProvider2` methods to edit the project's available platforms.  
  
     If a project does not support platforms, the platform column for that project displays None and is disabled.  
  
-   Build  
  
     Specifies whether or not the project is built by the current solution configuration. Unselected projects are not built when the solution-level build commands are invoked despite any project dependencies they contain. Projects not selected to be built are still included in debugging, running, packaging, and deployment of the solution.  
  
-   Deploy  
  
     Specifies whether or not the project will be deployed when the Start or Deploy commands are used with the selected solution build configuration. The check box for this field will be available if the project supports deploying by implementing the <xref:Microsoft.VisualStudio.Shell.Interop.IVsDeployableProjectCfg?qualifyHint=False> interface on its <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectCfg2?qualifyHint=False> object.  
  
 Once a new solution configuration is added, the user can select it from the Solution Configuration drop-down list box on the standard toolbar to build and/or start that configuration.  
  
## See Also  
 [Managing Configuration Options](../vs140/Managing-Configuration-Options.md)   
 [Project Configuration for Building](../vs140/Project-Configuration-for-Building.md)   
 [Project Configuration Object](../Topic/Project%20Configuration%20Object.md)