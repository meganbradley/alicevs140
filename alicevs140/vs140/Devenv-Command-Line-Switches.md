---
title: "Devenv Command Line Switches"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e12bc6ed-74fd-4bea-8d7c-89b99c20bad8
caps.latest.revision: 35
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Devenv Command Line Switches
Devenv lets you set various options for the integrated development environment (IDE), and also build, debug, and deploy projects, from the command line. Use these switches to run the IDE from a script or a .bat file, for example, a nightly build script, or to start the IDE in a particular configuration.  
  
> [!NOTE]
>  For build-related tasks, it is now recommended that you use MSBuild instead of devenv. For more information, see [MSBuild Command Line Reference](../vs140/MSBuild-Command-Line-Reference.md).  
  
> [!NOTE]
>  You must run devenv as an adminstrator in order to use the [/setup (devenv.exe)](../vs140/-Setup--devenv.exe-.md) and [/InstallVSTemplates (devenv.exe)](../vs140/-InstallVSTemplates--devenv.exe-.md) switches.  
  
## Devenv Switch Syntax  
 By default, devenv commands pass switches to the devenv.com utility.  
  
 The devenv.com utility provides for the delivery of output through standard system streams, such as `stdout` and `stderr`, and determines the appropriate I/O redirection when it captures output, for example, to a .txt file. Commands that begin instead with `devenv.exe` can use the same switches, but will send them to the devenv.exe program, bypassing the devenv.com utility.  
  
 The syntax rules for `devenv` switches resemble those for other DOS command-line utilities. The following syntax rules apply to all `devenv` switches and their arguments:  
  
-   Commands begin with `devenv`.  
  
-   Switches are not case-sensitive.  
  
-   When specifying a solution or project, the first argument is the name of the solution file or project file, including file path.  
  
-   If the first argument is a file that is not a solution or project, that file will open in the appropriate editor, in a new instance of the IDE.  
  
-   When you supply a project file name instead of a solution file name, a `devenv` command will search the parent folder of the project file for a solution file that has the same name. For example, the command `devenv /build myproject1.vbproj` will search the parent folder for a solution file that is named "myproject1.sln".  
  
    > [!NOTE]
    >  One and only one solution file that references this project should be located in its parent folder. If the parent folder contains no solution file that references this project, or if the parent folder contains two or more solution files that reference it, then a temporary solution file will be created that is named for this project and references it.  
  
-   When file paths and file names include spaces, you must enclose them in double quotation marks (""). For example, "c:\project a\\".  
  
-   Insert one space character between switches and arguments on the same line. For example, the command **devenv /log output.txt** opens the IDE and outputs all log information for that session to output.txt.  
  
-   You cannot use pattern-matching syntax in `devenv` commands.  
  
## Devenv Switches  
 Use the following command-line switches to display the IDE and perform the described task.  
  
|Command line switch|Description|  
|-------------------------|-----------------|  
|[/Command (devenv.exe)](../vs140/-Command--devenv.exe-.md)|Starts the IDE and executes the specified command.|  
|[/DebugExe (devenv.exe)](../vs140/-DebugExe--devenv.exe-.md)|Loads a [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] executable under the control of the debugger. This switch is not available for [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] or [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] executables. For more information, see [Automatically start a process in the debugger](../vs140/Debug-Multiple-Processes.md#BKMK_Automatically_start_an_process_in_the_debugger).|  
|[/LCID (devenv.exe)](../vs140/-LCID--devenv.exe-.md) or `/l`|Sets the default language for the IDE. If the specified language is not included in your installation of Visual Studio, this setting will be ignored.|  
|[/Log (devenv.exe)](../vs140/-Log--devenv.exe-.md)|Starts [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] and logs all activity to the log file.|  
|[/Run (devenv.exe)](../vs140/-Run--devenv.exe-.md) or `/r`|Compiles and runs the specified solution.|  
|[/Runexit (devenv.exe)](../vs140/-Runexit--devenv.exe-.md)|Compiles and runs the specified solution, minimizes the IDE when the solution is run, and closes the IDE after the solution has finished running.|  
|[/UseEnv (devenv.exe)](../vs140/-UseEnv--devenv.exe-.md)|Causes the IDE to use PATH, INCLUDE, and LIB environment variables for [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] compilation instead of the settings specified in the VC++ Directories section of **Projects** options in the **Options** dialog box. For more information, see [Setting the Path and Environment Variables for Command-Line Builds](../vs140/Setting-the-Path-and-Environment-Variables-for-Command-Line-Builds.md)|  
|[/Edit (devenv.exe)](../vs140/-Edit--devenv.exe-.md)|Opens the specified files in a running instance of this application. If there are no running instances, it will start a new instance with a simplified window layout.|  
|[/ResetAddin (devenv.exe)](../vs140/-ResetAddin--devenv.exe-.md)|Starts an instance of the Visual Studio IDE without loading the specified Add-in.|  
|[/SafeMode (devenv.exe)](../vs140/-SafeMode--devenv.exe-.md)|Starts [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] in safe mode, and loads only the default environment and services, and shipped versions of third-party packages.|  
|[/ResetSkipPkgs (devenv.exe)](../vs140/-ResetSkipPkgs--devenv.exe-.md)|Clears all SkipLoading tags that have been added to VSPackages by users who want to avoid loading problem VSPackages.|  
|[/setup (devenv.exe)](../vs140/-Setup--devenv.exe-.md)|Forces Visual Studio to merge resource metadata that describes menus, toolbars, and command groups, from all VSPackages available.|  
  
 Use the following command line switches to perform the described task. These command-line switches do not display the IDE.  
  
|Command line switch|Description|  
|-------------------------|-----------------|  
|[/? (devenv.exe)](../vs140/----devenv.exe-.md)|Displays help for devenv switches in the **Command Prompt window**.<br /><br /> **Devenv /?**|  
|[/Build (devenv.exe)](../vs140/-Build--devenv.exe-.md)|Builds the specified solution or project according to the configuration of the specified solution.<br /><br /> **Devenv myproj.csproj /build**|  
|[/Clean (devenv.exe)](../vs140/-Clean--devenv.exe-.md)|Deletes any files created by the build command, without affecting source files.<br /><br /> **Devenv myproj.csproj /clean**|  
|[/Deploy (devenv.exe)](../vs140/-Deploy--devenv.exe-.md)|Builds the solution, along with files necessary for deployment, according to the solutions configuration.<br /><br /> **Devenv myproj.csproj /deploy**|  
|[/Diff](../vs140/-Diff.md)|Compares two files.  Takes four parameters:SourceFile, TargetFile, SourceDisplayName(optional),TargetDisplayName(optional).|  
|[/InstallVSTemplates (devenv.exe)](../vs140/-InstallVSTemplates--devenv.exe-.md)|Registers project or item templates that are located in *<VisualStudioInstallDir\>*\Common7\IDE\ProjectTemplates or *<VisualStudioInstallDir\>*\Common7\IDE\ItemTemplates so that they can be accessed through the **New Project** and **Add New Item** dialog boxes.<br /><br /> **Devenv /InstallVSTemplates**|  
|[/Out (devenv.exe)](../vs140/-Out--devenv.exe-.md)|Lets you specify a file to receive errors when you build.<br /><br /> **Devenv myproj.csproj /build /out log.txt**|  
|[/Project (devenv.exe)](../vs140/-Project--devenv.exe-.md)|The project to build, clean, or deploy. You can use this switch only if you have also supplied the /build, /rebuild, /clean, or /deploy switch.|  
|[/ProjectConfig (devenv.exe)](../vs140/-ProjectConfig--devenv.exe-.md)|Specifies the project configuration to build or deploy. You can use this switch only if you have also supplied the /project switch.|  
|[/Rebuild (devenv.exe)](../vs140/-Rebuild--devenv.exe-.md)|Cleans and then builds the specified solution or project according to the configuration of the specified solution.|  
|[/ResetSettings (devenv.exe)](../vs140/-ResetSettings--devenv.exe-.md)|Restores Visual Studio default settings. Optionally resets the settings to the specified .vssettings file.|  
|[/Updateconfiguration](../vs140/-Updateconfiguration--devenv.exe-.md)|Notifies [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] to merge the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] packages on the system and check the MEF cache for any changes.|  
|[/Upgrade (devenv.exe)](../vs140/-Upgrade--devenv.exe-.md)|Upgrades the specified solution file and all its project files, or the specified project file, to the current [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] formats for these files.|  
  
## See Also  
 [General, Environment, Options Dialog Box](../vs140/General--Environment--Options-Dialog-Box.md)