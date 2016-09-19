---
title: "Getting Started with Language Service and Editor Extensions"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6b151891-c06d-40b1-9867-42298caa8492
caps.latest.revision: 23
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Getting Started with Language Service and Editor Extensions
You can use editor extensions to add language service features such as outlining, brace matching, IntelliSense, and light bulbs to your own programming language or to any content type. You can also customize the appearance and behavior of the Visual Studio editor, for example text coloring, margins, adornments, and other visual elements. You can also define your own type of content, and specify the appearance and behavior of the text views in which your content appears.  
  
 To get started writing editor extensions, use the editor project templates that are installed as part of the Visual Studio SDK. The Visual Studio SDK is a downloadable set of tools that make it easier to develop Visual Studio extensions, either by using VSPackages or by using the Managed Extensibility Framework (MEF).  
  
> [!NOTE]
>  For more information about the Visual Studio SDK, see [Visual Studio Integration SDK](../vs140/Visual-Studio-SDK.md).  
  
 We recommend that you learn about the following concepts and technologies before you write your own editor extensions.  
  
## The Windows Presentation Foundation (WPF) and Editor Extensions  
 The Visual Studio editor user interface (UI) is implemented by using the Windows Presentation Foundation (WPF). The WPF provides a rich visual experience and a consistent programming model that separates the visual aspects of the code from the business logic. You can use many WPF elements and features when you create editor extensions. For more information, see [Windows Presentation Foundation](assetId:///f667bd15-2134-41e9-b4af-5ced6fafab5d).  
  
## The Managed Extensibility Framework (MEF) and Editor Extensions  
 The Visual Studio editor uses the Managed Extensibility Framework (MEF) to manage its components and extensions. The MEF also lets developers more easily create extensions for a host application like Visual Studio. In this framework, you define an extension according to a MEF contract and export it as a MEF component part. The host application manages the component parts by finding them, registering them, and making sure that they are applied to the correct context.  
  
> [!NOTE]
>  For more information about the MEF in the editor, see [The Managed Extensibility Framework in the Editor](../vs140/Managed-Extensibility-Framework-in-the-Editor.md).  
  
## Visual Studio Editor Extension Points and Extensions  
 Editor extension points are MEF component parts that you can customize and extend. In some cases you extend the extension point by implementing an interface and exporting it together with the correct metadata. In other cases you just declare an extension and export it as a particular type.  
  
 The following are some of the basic kinds of editor extensions:  
  
-   Margins and scrollbars  
  
-   Tags  
  
-   Adornments  
  
-   Options  
  
-   IntelliSense  
  
 For more information about editor extension points, see [Editor Extension Points](../Topic/Language%20Service%20and%20Editor%20Extension%20Points.md).  
  
## Deploying Editor Extensions  
 In Visual Studio, you deploy editor extensions by adding a metadata file named source.extension.vsixmanifest to the solution, building the solution, and then adding a copy of the binary files and the manifest in a folder that is known to Visual Studio. The manifest file defines the basic facts about the extension (for example, name, author, version, and type of content). For more information about the VSIX manifest file and how to deploy extensions, see [VSIX Deployment](../vs140/Shipping-Visual-Studio-Extensions.md).  
  
 When you install an extension on a computer, include the binaries and the manifest in a subfolder of folder that is known to Visual Studio.  
  
> [!WARNING]
>  You do not have to worry about the details of manifests and deployment locations if you use one of the editor extensibility templates that are included in Visual Studio. The templates contain everything that is required to register and deploy an extension.  
  
## Running Extensions in the Experimental Instance  
 You can insulate your working version of Visual Studio while you are developing an extension by deploying it in the following experimental folder (on Windows Vista and Windows 7):  
  
 *%LOCALAPPDATA%*\VisualStudio\10.0Exp\Extensions\\*Company*\\*ExtensionID*  
  
 where *%LOCALAPPDATA%* is the name of the logged-on user, *Company* is the name of the company that owns the extension, and *ExtensionID* is the ID of the extension.  
  
 When you deploy an extension to the experimental location, it runs in debug mode. A second instance of Visual Studio is started, and is named **Microsoft Visual Studio - Experimental Instance**.  
  
## Managing extensions  
 Extensions to Visual Studio are listed in **Extensions and Updates** (on the **Tools** menu). If you are testing an extension in the experimental instance, it is listed in **Extensions and Updates** in the experimental instance, but is not listed in the development instance.  
  
 For more information, see [Managing Visual Studio Extensions](../vs140/Finding-and-Using-Visual-Studio-Extensions.md).  
  
## Using Templates to Create Editor Extensions  
 You can use editor templates to create MEF extensions that customize classifiers, adornments, and margins. There are templates for both C# and Visual Basic projects. For more information, see [Creating an Extension with an Editor Item Template](../vs140/Creating-an-Extension-with-an-Editor-Item-Template.md).  
  
 You can also use the VSIX Project template to create extensions. This template provides only the elements that are required to deploy any kind of extension, and include the source.extension.vsixmanifest file, the required assembly references, and a project file that includes the build tasks that allow you to deploy the extension. For more information, see [VSIX Project Template](../vs140/VSIX-Project-Template.md).  
  
 You can also create editor MEF components from a Visual Studio Package extension. See the following walkthroughs for details:  
  
-   [Walkthrough: How to Use a Shell Command to Add an Adornment](../Topic/Walkthrough:%20Using%20a%20Shell%20Command%20with%20an%20Editor%20Extension.md)  
  
-   [Walkthrough: How to Use an Access Key to Add an Adornment](../Topic/Walkthrough:%20Using%20a%20Shortcut%20Key%20with%20an%20Editor%20Extension.md)  
  
## See Also  
 [Editor Extension Points](../Topic/Language%20Service%20and%20Editor%20Extension%20Points.md)