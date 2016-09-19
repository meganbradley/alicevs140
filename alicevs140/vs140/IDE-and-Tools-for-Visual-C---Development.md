---
title: "IDE and Tools for Visual C++ Development"
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
ms.assetid: 56eabafb-1956-4f0f-bec5-29b887763559
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDE and Tools for Visual C++ Development
As part of the Visual Studio Integrated Development Environment (IDE), Visual C++ shares many windows and tools in common with other languages. Many of those, including **Solution Explorer**, the Code Editor, and the Debugger, are documented in the MSDN library under [Visual Studio IDE](../Topic/Visual%20Studio%20IDE.md). Often, a shared tool or window has a slightly different set of features for C++ than for the .NET languages or Javascript. Some windows or tools are only available in Visual Studio Pro or Visual Studio Enterprise. This topic introduces the Visual Studio IDE from the perspective of Visual C++, and provides links to other topics relevant to Visual C++.  
  
 In addition to shared tools in the Visual Studio IDE, Visual C++ has several tools specifically for native code development. These tools are also listed in this article. For a list of which tools are available in each edition of Visual Studio, see [Visual C++ Tools and Templates in Visual Studio Editions](../vs140/Visual-C---Tools-and-Templates-in-Visual-Studio-Editions.md).  
  
## Creating a solution and project(s)  
 In all editions of Visual C++, you organize the source code and related files for an executable ( such as an .exe, .dll or .lib) into a project. A project has a project file in XML format (.vcxproj) that specifies all the files and resources needed to compile the program, as well as other configuration settings, for example the target platform (x86, x64 or ARM) and whether you are building a release version or debug version of the program. A project (or many projects) are contained in a *Solution*; for example, a solution might contain several Win32 DLL projects, and a single Win32 console application that uses those DLLs. When you build the project, the MSBuild engine consumes the project file and produces the executable file and/or any other custom output you have specified.  
  
 **Project templates**  
  
 Visual C++ comes with several project templates, which contain starter code and the settings needed for a variety of basic program types. Typically you start by choosing **File &#124; New Project** to create a project from a project template, then add new source code files to that project, or start coding in the files provided. For information specific to C++ projects and project wizards, see [Creating and Managing Visual C++ Projects](../vs140/Creating-and-Managing-Visual-C---Projects.md).  
  
 **Application wizards**  
  
 Visual C++ provides wizards for some project types. A wizard guides you step-by-step through the process of creating a new project. This is useful for project types that have many options and settings. For more information, see [Creating Desktop Projects By Using Application Wizards](../vs140/Creating-Desktop-Projects-By-Using-Application-Wizards.md).  
  
## Creating user interfaces with designers  
 If your program has a user interface, one of the first tasks is to populate it with controls such as buttons, list boxes and so on. Visual Studio includes a visual design surface and a toolbox for each flavor of C++ application. No matter which type of app you are creating, the basic idea is the same: you drag a control from the toolbox window and drop it onto the design surface at the desired location. In the background, Visual Studio generates the resources and code required to make it all work.  
  
 For more information about designing a user interface for a Universal Windows Platform app, see  [Design and UI](https://developer.microsoft.com/en-us/windows/design).  
  
 For more information about creating a user interface for an MFC application, see [MFC Desktop Applications](../vs140/MFC-Desktop-Applications.md). For information about Win32 Windows programs, see [Win32 Windows Applications (C++)](../vs140/Windows-Desktop-Applications--C---.md).  
  
 For information about Windows Forms applications with C++/CLI, see [Creating a Windows Forms Application By Using the .NET Framework (C++)](assetId:///8e007885-6c8b-4fb2-a41d-91febd114a9b).  
  
## Writing and editing code  
 **Semantic colorization**  
  
 After you create a project, all the project files are displayed in the Solution Explorer window. When you click on a .h or .cpp file in Solution Explorer, the file opens up in the code editor. The code editor is a specialized word processor for C++ source code. It color-codes language keywords, method and variable names, and other elements of your code to make the code more readable and easier to understand.  
  
 **Intellisense**  
  
 The code editor also supports several features that together are known as Intellisense. You can hover over a method and see some basic documentation for it. After you type a class variable name and a . or ->, a list of instance members of that class appears. If you type a class name and then a ::, a list of static members appears. When you start typing a class or method name, the code editor will offer suggestions to complete the statement. For more information, see [Using IntelliSense](../vs140/Using-IntelliSense.md).  
  
 **Code snippets**  
  
 You can use Intellisense code snippets to generate commonly-used or complicated code constructs with a shortcut keystroke. For more information, see [Code Snippets](../vs140/Code-Snippets.md).  
  
## Navigating code  
 The VIEW menu provides access to many windows and tools for navigating around in your code files. For detailed information about these windows, see [Viewing the Structure of Code](../vs140/Viewing-the-Structure-of-Code.md).  
  
 **Solution Explorer**  
  
 In all editions of Visual Studio, use the Solution Explorer pane to navigate between the files in a project. Expand a .h or .cpp file icon to view the classes in the file. Expand a class to see its members. Double-click on a member to navigate to its definition or implementation in the file.  
  
 **Class View and Code Definition Window**  
  
 Use the Class View pane to see the namespaces and classes across all the files, including partial classes. You can expand each namespace or class to see its members and double-click on the member to navigate to that location in the source file. If you open the Code Definition Window, you can view the definition or implementation of the type when you choose it in Class View.  
  
 **Object Browser**  
  
 Use Object Browser to explore type information in Windows Runtime components (.winmd files), .NET assemblies and COM type libraries. It is not used with Win32 DLLs.  
  
 **Go To Definition/Declaration**  
  
 Press F12 on any API name or member variable to go to its definition. If the definition is in a .winmd file (for a [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] app) then you will be shown the type info in the Object Browser. You can also Go To Definition or Go To Declaration by right-clicking on the variable or type name and choosing the option from the context menu.  
  
 **Find All References**  
  
 In a source code file, right-click with the mouse cursor over the name of a type or method or variable, and choose Find all References to return a list of every location in the file, project or solution where the type is used. Find All References is intelligent and only returns instances of the same identical variable, even if other variables at different scope have the same name.  
  
 **Architecture Explorer and Dependency Graphs (Ultimate)**  
  
 Use Architecture Explorer to view relationships between various elements in your code. For more information, see [Find code with Architecture Explorer](assetId:///b1707926-ef73-47f9-92cd-e00d0fac7e76). Use  dependency graphs to view dependency relationships. For more information, see [How to: Generate Dependency Graphs for C and C++ Code](assetId:///3bd5cf9f-62f6-41d0-9f35-d4b2637cba3c).  
  
## Adding and Editing Resources  
 The term "resource" in the context of a Visual Studio desktop project includes things such as dialog boxes, icons, localizable strings, spash screens, database connection strings, or any arbitrary data that you want to include in the executable file.  
  
 For more information on adding and editing resources in native desktop C++ projects, see [Working with Resource Files](../vs140/Working-with-Resource-Files.md).  
  
## Building (compiling and linking)  
 Press **Ctrl + Shift + B** to compile and link a project. Visual Studio uses [MSBuild](../Topic/MSBuild.md) to create executable code. You can set general build options under **Tools &#124; Options &#124; Projects and Solutions** and you can set properties for specific projects under **Project &#124; Properties**. Build errors and warnings are reported in the Error List (**Ctrl +\\, E**). Additional information is sometimes shown in the Output Window (**Alt + 2**). For more information, see  [Working with Project Properties](../vs140/Working-with-Project-Properties.md) and [Building C++ Projects in Visual Studio](../vs140/Building-C---Projects-in-Visual-Studio.md).  
  
 You can also use the Visual C++ compiler (cl.exe) and many other build-related standalone tools such as NMAKE and LIB directly from the command line. For more information, see [Building on the Command Line](../vs140/Building-on-the-Command-Line.md) and [C/C++ Building Reference](../vs140/C-C---Building-Reference.md).  
  
## Testing  
 Visual Studio includes a unit test framework for both native C++ and C++/CLI. For more information, see [Verifying Code by Using Unit Tests](../Topic/Unit%20Test%20Your%20Code.md) and [Writing Unit tests for C/C++ with the Microsoft Unit Testing Framework for C++](../vs140/Writing-Unit-tests-for-C-C---with-the-Microsoft-Unit-Testing-Framework-for-C--.md)  
  
## Debugging  
 You can debug your program by pressing F5 when your project configuration is set to Debug. While debugging you can set breakpoints by pressing F9, step through code by pressing F10, view the values of specified variables or registers, and even in some cases make changes in code and continue debugging without re-compiling. For more information, see [Debugging in Visual Studio](../vs140/Debugging-in-Visual-Studio.md).  
  
## Deploying completed applications  
 You deploy a [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] to customers through the Windows Store through the **PROJECT &#124; Store** menu option. Deployment of the CRT is handled automatically behind the scenes. For more information, see [Selling Apps](http://go.microsoft.com/fwlink/p/?LinkId=262280).  
  
 When you deploy a native C++ desktop application to another computer, you must install the application itself and any library files that the application depends on. There are three ways to deploy the Visual C++ runtime with an application: central deployment, local deployment, or static linking. For more information, see [Deploying Native Desktop Applications (Visual C++)](../vs140/Deploying-Native-Desktop-Applications--Visual-C---.md).  
  
 For more information about deploying a C++/CLI program, see [.NET Framework Deployment Guide for Developers](assetId:///094d043e-33c4-40ba-a503-e0b20b55f4cf),  
  
## Other tools  
  
## Related Articles  
  
|||  
|-|-|  
|[Visual C++ Tools and Templates in Visual Studio Editions](../vs140/Visual-C---Tools-and-Templates-in-Visual-Studio-Editions.md)|Shows which features are available in the various editions of Visual Studio.|  
|[Visual C++ Guided Tour](assetId:///499cb66f-7df1-45d6-8b6b-33d94fd1f17c)|Provides an overview of the Visual Studio development environment and the kinds of C++ apps that you can create.|  
|[Creating and Managing Visual C++ Projects](../vs140/Creating-and-Managing-Visual-C---Projects.md)|Provides an overview of C++ projects in Visual Studio and links to other articles that explain how to create and manage them.|  
|[Building C/C++ Programs](../vs140/Building-C-C---Programs.md)|Describes how to build C++ projects.|  
|[Deploying Desktop Applications](../vs140/Deploying-Native-Desktop-Applications--Visual-C---.md)|Provides an overview of deployment for C++ apps and links to other articles that describe deployment in detail.|  
|[Porting and Upgrading Programs](assetId:///c36c44b3-5a9b-4bb4-9b7a-469aa770ed00)|Links to articles that describe how to open C++ apps that were created in earlier versions of Visual Studio, and also how to open apps that were created by using tools other than Visual Studio.|  
|||  
|[Visual C++](../vs140/Visual-C---in-Visual-Studio-2015.md)|Describes key features of Visual C++ in Visual Studio and links to the rest of the Visual C++ documentation.|