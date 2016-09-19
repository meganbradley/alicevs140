---
title: "Walkthrough: Building an Application"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4842955d-8959-4e4e-98b8-2358360179b3
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Walkthrough: Building an Application
By completing this walkthrough, you’ll  become more familiar with several options that you can configure when you build applications with Visual Studio. You’ll create a custom build configuration, hide certain warning messages, and increase build output information, among other tasks, for a sample application.  
  
 This topic contains the following sections:  
  
 [Install the Sample Application](../vs140/Walkthrough--Building-an-Application.md#BKMK_installapp)  
  
 [Create a Custom Build Configuration](../vs140/Walkthrough--Building-an-Application.md#BKMK_CreateBuildConfig)  
  
 [Build the Application](../vs140/Walkthrough--Building-an-Application.md#BKMK_building)  
  
 [Hide Compiler Warnings](../vs140/Walkthrough--Building-an-Application.md#BKMK_hidewarning)  
  
 [Display Additional Build Details in the Output Window](../vs140/Walkthrough--Building-an-Application.md#BKMK_outputdetails)  
  
 [Create a Release Build](../vs140/Walkthrough--Building-an-Application.md#BKMK_releasebuild)  
  
##  <a name="BKMK_installapp"></a> Install the Sample Application  
 You’ll use the **Extensions and Updates** dialog box to find and install the [Introduction to Building WPF Applications](http://code.msdn.microsoft.com/Introduction-to-Building-b8d16419?SRC=VSIDE) sample from the Samples Gallery on the Microsoft website. The Samples Gallery provides a variety of example projects and code that you can download and review as you plan and develop your applications.  
  
#### To install the sample application  
  
1.  On the menu bar, choose **Tools**, **Extensions and Updates**.  
  
2.  Choose the **Online** category, and then choose the **Samples Gallery** category.  
  
3.  Specify `Introduction` in the search box to find the sample.  
  
     ![Extensions and Updates dialog box](../vs140/media/BuildWalk_ExtensionsDialogSampleDownload.png "BuildWalk_ExtensionsDialogSampleDownload")  
  
4.  In the results list, choose either **Introduction to Building WPF Applications (Visual C#)** or **Introduction to Building WPF Applications (Visual Basic)**.  
  
5.  Choose the **Download** button, and then choose the **Close** button.  
  
 The Introduction to Building WPF Applications sample appears in the **New Project** dialog box.  
  
#### To create a solution for the sample application  
  
1.  Open the **New Project** dialog box.  
  
     ![On the menu bar, choose File, New, Project](../vs140/media/ExploreIDE-FileNewProject.png "ExploreIDE-FileNewProject")  
  
2.  In the **Installed** category, choose the **Samples** category to display the Introduction to Building WPF Applications sample.  
  
3.  Name the solution `IntroWPFcsharp` for Visual C#.  
  
     ![New Project dialog box, Installed Samples](../vs140/media/BuildWalk_NewProjectdlgIntrotoWPFsample.png "BuildWalk_NewProjectdlgIntrotoWPFsample")  
  
     OR  
  
     Name the solution `IntroWPFvb` for Visual Basic.  
  
     ![New Project dialog box, Visual Basic Sample](../vs140/media/BuildWalk_NewProjectdlgIntrotoWPFsampleVB.png "BuildWalk_NewProjectdlgIntrotoWPFsampleVB")  
  
4.  Choose the **OK** button.  
  
##  <a name="BKMK_CreateBuildConfig"></a> Create a Custom Build Configuration  
 When you create a solution, debug and release build configurations and their default platform targets are defined for the solution automatically. You can then customize these configurations or create your own. Build configurations specify the build type. Build platforms specify the operating system that an application targets for that configuration. For more information, see [Understanding Build Configurations](../vs140/Understanding-Build-Configurations.md), [Understanding Build Platforms](../vs140/Understanding-Build-Platforms.md), and [Debug and Release Project Configurations](assetId:///0440b300-0614-4511-901a-105b771b236e).  
  
 You can change or create configurations and platform settings by using the **Configuration Manager** dialog box. In this procedure, you’ll create a build configuration for testing.  
  
#### To create a build configuration  
  
1.  Open the **Configuration Manager** dialog box.  
  
     ![Build menu, Configuration Manager command](../vs140/media/BuildWalk_ConfigurationManagerDialogBox.png "BuildWalk_ConfigurationManagerDialogBox")  
  
2.  In the **Active solution configuration** list, choose **New**.  
  
3.  In the **New Solution Configuration** dialog box, name the new configuration `Test`, copy settings from the existing Debug configuration, and then choose the **OK** button.  
  
     ![New Solution Configuration Dialog Box](../vs140/media/BuildWalk_NewSolutionConfigDlgBox.png "BuildWalk_NewSolutionConfigDlgBox")  
  
4.  In the **Active solution platform** list, choose **New**.  
  
5.  In the **New Solution Platform** dialog box, choose**x64**, and don’t copy settings from the x86 platform.  
  
     ![New Solution Platform Dialog Box](../vs140/media/BuildWalk_NewSolutionPlatform.png "BuildWalk_NewSolutionPlatform")  
  
6.  Choose the **OK** button.  
  
 The active solution configuration has been changed to Test with the active solution platform set to x64.  
  
 ![Configuration Manager with Test configuration](../vs140/media/BuildWalk_ConfigManagerTestconfig.png "BuildWalk_ConfigManagerTestconfig")  
  
 You can quickly verify or change the active solution configuration by using the **Solution Configurations** list on the **Standard** toolbar.  
  
 ![Solution Configuration option Standard Toolbar](../vs140/media/BuildWalk_StandardToolbarSolutionCongfig.png "BuildWalk_StandardToolbarSolutionCongfig")  
  
##  <a name="BKMK_building"></a> Build the Application  
 Next, you’ll build the solution with the custom build configuration.  
  
#### To build the solution  
  
-   On the menu bar, choose **Build**, **Build Solution**.  
  
 The **Output** window displays the results of the build. The build succeeded, but several warning messages were generated.  
  
 Figure 1: Visual Basic warnings  
  
 ![Output Window Visual Basic](../vs140/media/BuildWalk_VBBuildOutputWnd.png "BuildWalk_VBBuildOutputWnd")  
  
 Figure 2: Visual C# warnings  
  
 ![Output Window Visual C&#35;](../vs140/media/BuildWalk_CsharpBuildOutputWnd.png "BuildWalk_CsharpBuildOutputWnd")  
  
##  <a name="BKMK_hidewarning"></a> Hide Compiler Warnings  
 You can temporarily hide certain warning messages during a build rather than have them clutter up the build output.  
  
#### To hide a specific Visual C# warning  
  
1.  In **Solution Explorer**, choose the top-level project node.  
  
2.  On the menu bar, choose **View**, **Property Pages**.  
  
     The **Project Designer** opens.  
  
3.  Choose the **Build** page and then, in the **Suppress warnings** box, specify the warning number `1762`.  
  
     ![Build page, Project Designer](../vs140/media/BuildWalk_CsharpSupressWarnings.png "BuildWalk_CsharpSupressWarnings")  
  
     For more information, see [Build Page, Project Designer (C#)](../Topic/Build%20Page,%20Project%20Designer%20\(C%23\).md).  
  
4.  Build the solution.  
  
     The **Output** window displays only summary information for the build.  
  
     ![Output Window, Visual C&#35; Build Warnings](../vs140/media/BuildWalk_VisualCsharpBuildWarnings.png "BuildWalk_VisualCsharpBuildWarnings")  
  
#### To suppress all Visual Basic build warnings  
  
1.  In **Solution Explorer**, choose the top-level project node.  
  
2.  On the menu bar, choose **View**, **Property Pages**.  
  
     The **Project Designer** opens.  
  
3.  On the **Compile** page, select the **Disable all warnings** check box.  
  
     ![Compile page, Project Designer](../vs140/media/BuildWalk_VBSupressWarnings.png "BuildWalk_VBSupressWarnings")  
  
     For more information, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
4.  Build the solution.  
  
 The **Output** window displays only summary information for the build.  
  
 ![Output Window, Visual Basic Build Warnings](../vs140/media/BuildWalk_VisualBasicBuildWarnings.png "BuildWalk_VisualBasicBuildWarnings")  
  
 For more information, see [How to: Suppress Compiler Warnings](../vs140/How-to--Suppress-Compiler-Warnings.md).  
  
##  <a name="BKMK_outputdetails"></a> Display Additional Build Details in the Output Window  
 You can change how much information about the build process appears in the **Output** window. Build verbosity is usually set to Minimal, which means that the **Output** window displays only a summary of the build process along with any high priority warnings or errors. You can display more information about the build by using the [Build and Run, Projects and Solutions, Options Dialog Box](../vs140/Options-Dialog-Box---Projects-and-Solutions--Build-and-Run.md).  
  
> [!IMPORTANT]
>  If you display more information, the build will take longer to complete.  
  
#### To change the amount of information in the Output window  
  
1.  Open the **Options** dialog box.  
  
     ![Options command on the Tools menu](../vs140/media/ExploreIDE-ToolsOptionsmenu.png "ExploreIDE-ToolsOptionsmenu")  
  
2.  Choose the **Projects and Solutions** category, and then choose the **Build and Run** page.  
  
3.  In the **MSBuild project build output verbosity** list, choose **Normal**, and then choose the **OK** button.  
  
4.  On the menu bar, choose **Build**, **Clean Solution**.  
  
5.  Build the solution, and then review the information in the **Output** window.  
  
     The build information includes the time that the build started (located at the beginning), the order in which files were processed, and the amount of time that the process took to complete (located at the end). This information also includes the actual compiler syntax that Visual Studio runs during the build.  
  
     For example, in the Visual C# build, the [/nowarn](../vs140/-nowarn.md) option lists the warning code, 1762, that you specified earlier in this topic, along with three other warnings.  
  
     In the Visual Basic build, [/nowarn](../vs140/-nowarn.md) doesn’t include specific warnings to exclude, so no warnings appear.  
  
    > [!TIP]
    >  You can search the contents of the **Output** window if you display the **Find** dialog box by choosing the Ctrl+F keys.  
  
 For more information, see [How to: View, Save, and Configure Build Log Files](../Topic/How%20to:%20View,%20Save,%20and%20Configure%20Build%20Log%20Files.md).  
  
##  <a name="BKMK_releasebuild"></a> Create a Release Build  
 You can build a version of the sample application that’s optimized for shipping it. For the release build, you’ll specify that the executable is copied to a network share before the build is kicked off.  
  
 For more information, see [How to: Change the Build Output Directory](../vs140/How-to--Change-the-Build-Output-Directory.md) and [Building and Cleaning Projects and Solutions in Visual Studio](../vs140/Building-and-Cleaning-Projects-and-Solutions-in-Visual-Studio.md).  
  
#### To specify a release build for Visual Basic  
  
1.  Open the **Project Designer**.  
  
     ![View menu, Property Pages command](../vs140/media/BuildWalk_ViewPropertyPages.png "BuildWalk_ViewPropertyPages")  
  
2.  Choose the **Compile** page.  
  
3.  In the **Configuration** list, choose **Release**.  
  
4.  In the **Platform** list, choose **x86**.  
  
5.  In the **Build output path** box, specify a network path.  
  
     For example, you can specify \\\myserver\builds.  
  
    > [!IMPORTANT]
    >  A message box might appear, warning you that the network share that you’ve specified might not be a trusted location. If you trust the location that you’ve specified, choose the **OK** button in the message box.  
  
6.  Build the application.  
  
     ![Build Solution command on the Build menu](../vs140/media/ExploreIDE-BuildSolution.png "ExploreIDE-BuildSolution")  
  
#### To specify a release build for Visual C#  
  
1.  Open the **Project Designer**.  
  
     ![View menu, Property Pages command](../vs140/media/BuildWalk_ViewPropertyPages.png "BuildWalk_ViewPropertyPages")  
  
2.  Choose the **Build** page.  
  
3.  In the **Configuration** list, choose **Release**.  
  
4.  In the **Platform** list, choose **x86**.  
  
5.  In the **Output path** box, specify a network path.  
  
     For example, you could specify \\\myserver\builds.  
  
    > [!IMPORTANT]
    >  A message box might appear, warning you that the network share that you’ve specified might not be a trusted location. If you trust the location that you’ve specified, choose the **OK** button in the message box.  
  
6.  Build the application.  
  
     ![Build Solution command on the Build menu](../vs140/media/ExploreIDE-BuildSolution.png "ExploreIDE-BuildSolution")  
  
 The executable file is copied to the network path that you specified. Its path would be \\\myserver\builds\\*FileName*.exe.  
  
 Congratulations: you’ve successfully completed this walkthrough.  
  
## See Also  
 [Walkthrough: Building a Project (C++)](../vs140/Walkthrough--Building-a-Project--C---.md)   
 [ASP.NET Web Application Project Precompilation Overview](assetId:///b940abbd-178d-4570-b441-52914fa7b887)   
 [Walkthrough: Using MSBuild](../vs140/Walkthrough--Using-MSBuild.md)