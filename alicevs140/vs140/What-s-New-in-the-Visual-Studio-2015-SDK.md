---
title: "What&#39;s New in the Visual Studio 2015 SDK"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c64aac80-a411-463f-b7bd-8b7607a52ece
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# What&#39;s New in the Visual Studio 2015 SDK
The Visual Studio SDK has the following new and updated features for Visual Studio 2015, Visual Studio 2015 updated, and Visual Studio "15".  
  
## Visual Studio "15" Preview 2  
 Starting in Visual Studio "15" Preview 4, scanning for custom project and item templates will no longer be performed. Instead, the extension must provide template manifest files that describe the install location of these templates. You can use the Preview 2 installation to update your VSIX extensions. If you deploy your extension using an MSI, you must generate the template manifest files by hand. For more information, see [Upgrading Custom Project and Item Templates for Visual Studio “15”](../vs140/Upgrading-Custom-Project-and-Item-Templates-for-Visual-Studio-“15”.md). The template manifest schema is documented in [Visual Studio Template Manifest Schema Reference](../vs140/Visual-Studio-Template-Manifest-Schema-Reference.md).  
  
## VS 2015 SDK Update 1  
 Update 1 includes tools to help your extension work well with color themes and the Visual Studio image service.  
  
 These topics are under the [VS SDK Utilities](../vs140/VSSDK-Utilities.md) section:  
  
-   The [Color Theming Tools](../vs140/Color-Theming-Tools.md) help you create and edit custom colors for Visual Studio.  
  
-   The [Image Service Tools](../vs140/Image-Service-Tools.md) let you work with Visual Studio image manifest files.  
  
## New Way to Add the Visual Studio SDK to Visual Studio  
 Starting in Visual Studio 2015, you don't need to download the Visual Studio SDK separately. Instead, you can install it as part of the normal installation process, or you can choose to install it later on. When you open or create  a VSIX solution, Visual Studio will ask you to install the Visual Studio Extensibility Tools. For more information, see [Installing the Visual Studio SDK](../vs140/Installing-the-Visual-Studio-SDK.md).  
  
## New Ways of Creating Extensions  
 Starting in the Visual Studio 2015 SDK, you have different options for creating extensions, depending on which programming language you’re using.  
  
### Visual C# and Visual Basic  
 For C# and Visual Basic, there is a full range of project item templates that allow you to create VSPackages, menu commands, tool windows, editor classifiers, editor adornments, and editor margin extensions. You can add any or all of these to the standard VSIX project. For more information, see:  
  
-   [Creating an Extension with a Menu Command](../Topic/Creating%20an%20Extension%20with%20a%20Menu%20Command.md)  
  
-   [Creating an Extension with a Tool Window](../vs140/Creating-an-Extension-with-a-Tool-Window.md)  
  
-   [Creating an Extension with an Editor Item Template](../vs140/Creating-an-Extension-with-an-Editor-Item-Template.md)  
  
-   [Creating an Extension with a VSPackage](../vs140/Creating-an-Extension-with-a-VSPackage.md)  
  
     The VSPackage Wizard no longer creates extensions in C# or Visual Basic.  
  
### C++  
 For C++, the VSPackage Wizard support menu commands, tool windows, and custom editors. Look for it in the **New Project** dialog in **Visual C++ / Extensibility**.  
  
## VS SDK Reference Assemblies via NuGet  
 For increased portability and sharing of extensibility projects, you can use the NuGet versions of the VS SDK reference assemblies.  These are available on [nuget.org](http://www.nuget.org) published by [VisualStudioExtensibility](http://www.nuget.org/profiles/VisualStudioExtensibility) and can be easily added to your project or solution through the Visual Studio **References / Manage NuGet Packages** dialog. You can add individual references to specific extensibility assemblies or add all the VS SDK references assemblies at once using the VS SDK [Meta package](http://www.nuget.org/packages/VSSDK_Reference_Assemblies). To learn more about NuGet, see [NuGet Overview](http://docs.nuget.org/) and [Manage NuGet Packages Using the Dialog](http://docs.nuget.org/Consume/Package-Manager-Dialog).  
  
 When you use the NuGet versions of the VS SDK reference assemblies, another user doesn’t need to install the VS SDK to open and build your project.  The NuGet reference assemblies and VS SDK build tools will automatically be installed on their computer for that project.  
  
 The VS SDK item templates use NuGet for their references and build tools so you get the benefits of NuGet by default.  
  
> [!NOTE]
>  You can continue to use the VS SDK installed reference assemblies with your projects (located under <Visual Studio Install Location\>\ VSSDK\VisualStudioIntegration\Common\Assemblies) and existing extensibility projects do not need to be upgraded to use NuGet packages.  The project **References / Add Reference** dialog continues to use the VS SDK installed reference assemblies.  
>   
>  If you’d like to modify your existing projects to use NuGet, see [How to: Migrate VSPackages to Visual Studio 2015](../vs140/How-to--Migrate-Extensibility-Projects-to-Visual-Studio-2015.md) which has a section on updating extensibility projects to NuGet packages.  
  
## Light Bulbs  
 One of the most exciting new ways of writing extension code is provided by the Roslyn project. For more information, see [Roslyn](https://github.com/dotnet/Roslyn).  
  
 Light bulbs are a new feature that ships with the VSSDK. They are icons used in the Visual Studio editor that expand to display a set of code refactoring actions or fixes for problems identified by the built-in code analyzers. For more information, see [Walkthrough: Displaying Light Bulb Suggestions](../Topic/Walkthrough:%20Displaying%20Light%20Bulb%20Suggestions.md).  
  
## Updated User Experience Guidelines  
 Designing new extensions or features for Visual Studio? Check out the updated and expanded [Visual Studio User Experience Guidelines](../vs140/Visual-Studio-User-Experience-Guidelines.md).  You’ll find the [color tokens](../vs140/Shared-Colors-for-Visual-Studio.md), [font sizes](../vs140/Fonts-and-Formatting-for-Visual-Studio.md), [dialog layout specifications](../vs140/Layout-for-Visual-Studio.md), and other guidance you need to seamlessly integrate your new UI with Visual Studio.