---
title: "Using Visual Studio to Write F# Programs"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: f179937e-e9b5-403d-bc8c-9c78cc433e8f
caps.latest.revision: 31
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using Visual Studio to Write F# Programs
The Visual Studio Integrated Development Environment (IDE) includes support for F#, including code editing, IntelliSense, debugging, and features that assist in packaging and deploying applications. Visual F# supports many of the features supported in other .NET Framework languages.  
  
## Scripts and Projects Compared  
 There are two basic styles of development that Visual F# supports: scripts and projects. You can use an F# script when you just want to run a small amount of code that you do not want to make into a permanent application. You use a project when you are creating a more permanent application.  
  
 To create and run an F# script, you do not need to create a project. To create an F# script, on the **File** menu, point to **New** and then click **File**. In the **New File** dialog box, select **Script** in the **Installed Templates** list, and then select **F# Script File**. Scripts are designed for execution with F# Interactive (fsi.exe). For more information, see [F# Interactive (fsi.exe) Reference](../Topic/F%23%20Interactive%20\(fsi.exe\)%20Reference.md).  
  
## Projects and Solutions  
 Projects include a collection of files that produce a single assembly. Projects are designed for compilation with fsc.exe and can be run in the Visual Studio debugger. The assembly that is produced can be an executable file or a library (DLL). A project consists of source files all written in the same programming language. A *solution* is a collection of projects. Projects in a solution can be written in different languages. For example, you can have a Visual Basic or C# user interface for your application, which is one project, and an F# library as another project. One of these projects will be the startup project: the one that is set to run when you start the application.  
  
 To create an F# project, on the **File** menu, point to **New** and then click **Project**. In the **New Project** dialog box, select a project template. [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] provides templates that enable you to create projects that already have all the basic elements and settings that support applications and libraries.  
  
 When you deploy your applications to run on computers other than your development computer, you must specify a deployment option, and make sure that the F# runtime is included in the deployment. For a full description of deployment options, see [Deploying Applications and Components](../vs140/Deploying-Applications--Services--and-Components.md).  
  
## Round-Tripping Projects in Visual Studio  
 You can open and work with F# projects that were created in [!INCLUDE[vs_dev12](../vs140/includes/vs_dev12_md.md)] or [!INCLUDE[vs_dev11_long](../vs140/includes/vs_dev11_long_md.md)] in either version of Visual Studio, without making any modifications. The only exception is that, the first time that you open a [!INCLUDE[vs_dev11_long](../vs140/includes/vs_dev11_long_md.md)] project in [!INCLUDE[vs_dev12](../vs140/includes/vs_dev12_md.md)], Visual Studio makes a small change to enable the project to be used in both versions. This capability is known as round-tripping.  
  
 You can specify which version of the F# runtime (and core library) you want to target on the **Application** tab of the project’s properties. Choose **F# 3.0** if you’re creating a library that must run in many contexts or you want to participate in project round-tripping. If you choose **F# 3.0**, you won't be able to use any of the language features that are new in F# 3.1, such as named union cases and enhanced array slicing. If you change the target runtime to **F# 3.1**, you can’t reopen the project in [!INCLUDE[vs_dev11_long](../vs140/includes/vs_dev11_long_md.md)].  
  
## Creating Applications That Have User Interfaces  
 Other languages support visual designers that enable you to create UIs for applications. F# programs can directly target the .NET Framework libraries, such as WPF, Windows Forms, or ASP.NET, that enable you to create UIs for applications in F#, but [!INCLUDE[vs_dev11_long](../vs140/includes/vs_dev11_long_md.md)] does not provide a visual designer to help you create interfaces. A typical scenario is to create a multiple-language solution with one Visual Basic or C# application project that contains the UI, and also have one or more F# library projects.  
  
## F# Projects  
 The order of files is significant in F# projects. Files in an F# project are processed in order by the F# compiler. The F# compiler requires that you define all constructs before you start to use them; therefore, the files that include the definition of any F# construct must appear earlier in the list of files in the project than the files that use that construct. You also must avoid circular dependencies that span multiple files. To make it easier to move files around in a project, F# provides commands that enable you to move files up or down in the file list in **Solution Explorer**. You can access these commands by right-clicking the files in the file list or using the keyboard shortcuts, which are displayed on the menu.  
  
## F# Files in F# Projects  
 The following table summarizes some the file types that you can use in F# projects.  
  
|File type and extension|Description|  
|-----------------------------|-----------------|  
|Implementation file (.fs)|Used for F# code.|  
|Signature file (.fsi)|Used to specify the public signatures of modules and types in an F# implementation file. For more information, see [Signatures (F#)](../vs140/Signatures--F#-.md).|  
|Script (.fsx)|Used to include informal testing code in F# without adding the test code to your application, and without creating a separate project for it. By default, script files are not included in the build of a project even when they are part of a project.|  
  
## Portable Libraries in F#  
 You use the F# Library, the F# Portable Library, or the F# Portable Library (Legacy) project template when you create a DLL and the F# Application project when you create an executable file. You should use the F# Portable Library project if your library will be consumed by applications that use the Windows Runtime, such as a Windows Store app, or another platform that uses the .NET Framework 4.5. Use the F# Portable Library (legacy) project template if your library will be consumed by portable applications, such as Windows Store or Silverlight 5 apps, that can run on the .NET Framework 4. You can also target Silverlight by using the Silverlight project template.  
  
> [!WARNING]
>  **Note** If your Visual C# app uses an F# portable library or legacy portable library, you must add a reference in your Visual C# project to the appropriate version of the F# Core Library (FSharp.Core.dll). To add a reference in your C# project, you must browse to the same version of FSharp.Core.dll that your F# library uses. To obtain the path, choose the FSharp.Core node in the **References** section of your F# project in **Solution Explorer** and then view the **Full Path** property in the **Properties** window.  
  
 The following table summarizes the choices for F# portable libraries.  
  
### F# Portable Libraries in [!INCLUDE[vs_dev12](../vs140/includes/vs_dev12_md.md)]  
  
|Project Template|.NET Portable Subset version|F# Core Library version|App types targeted|  
|----------------------|----------------------------------|------------------------------|------------------------|  
|Portable|4.5.0.0|3.3.1.0|.NET Framework 4.5 and Windows Store|  
|Portable Library (Legacy)<br /><br /> Silverlight Library|4.0.0.0|2.3.5.1|.NET Framework 4, Windows Store, and Silverlight|  
  
 Other versions of the F# Core Library on disk support projects that were created with older versions of Visual Studio. For example, if you created an F# portable library project in Visual Studio 2012 and open it in [!INCLUDE[vs_dev12](../vs140/includes/vs_dev12_md.md)], the version of FSharp.Core referenced would be 2.3.5.0.  
  
## Related Topics  
  
|Title|Description|  
|-----------|-----------------|  
|[F# Development Environment Features](../vs140/F#-Development-Environment-Features.md)|Lists [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] features and indicates which are supported in Visual F#.|  
|[Configuring Projects (F#)](../vs140/Configuring-Projects--F#-.md)|Provides information about project settings in Visual F#.|  
|[Projects, User Interface Elements](../vs140/Project-Properties-Reference.md)|Provides links to topics that describe Visual Studio dialog boxes that pertain to projects. F# project support is a subset of the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] support.|  
|[Visual F#](../vs140/Visual-F#.md)|Introduces Visual F# and provides links to relevant topics.|  
|[Walkthrough: Using Visual F# to Create, Debug and Deploy an Application](../Topic/Walkthrough:%20Using%20Visual%20F%23%20to%20Create,%20Debug,%20and%20Deploy%20an%20Application.md)|Provides step-by-step instructions for developing applications in Visual F#.|  
|[Debugging F#](../vs140/Debugging-F#.md)|Provides information about debugging in F#.|  
|[Visual F# Guided Tour](../vs140/Visual-F#-Guided-Tour.md)|Provides links to introductory tutorials for some aspects of programming in F#|