---
title: "Developing Visual Studio Extensions"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5b1b5db3-6005-44cf-83b0-e608d7764d14
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Developing Visual Studio Extensions
You have several alternatives to choose from when you decide to write an extension to Visual Studio.  
  
 If you want to integrate a large component into Visual Studio, for example, a new project system or a new programming language, you can create a Visual Studio package by using the Visual Studio SDK. If you want to create an application that is based on Visual Studio technology, you can create a Visual Studio isolated shell application. Both Visual Studio integrated extensions and Visual Studio isolated shell applications are based on VSPackages. For more information, see [VSPackages](../vs140/VSPackages.md).  
  
 Another extension mechanism, which is based on the Managed Extensibility Framework (MEF), lets you customize and extend the Visual Studio editor just by creating MEF component parts. You do not have to create and register a VSPackage to use these extensions. For more information, see [The Visual Studio Editor](../Topic/Extending%20the%20Editor%20and%20Language%20Services.md).  
  
## Visual Studio SDK Templates  
 When you install the Visual Studio SDK, a number of project templates are added to your Visual Studio installation.  
  
|Template|Location|Using the Template|  
|--------------|--------------|------------------------|  
|VSIX Project template|Visual Basic and Visual C# Extensibility|[Creating Extensions with the VSIX Project Template](../vs140/Getting-Started-with-the-VSIX-Project-Template.md)|  
|Editor templates|Visual Basic and Visual C# Extensibility|[Using Editor Templates to Create Extensions](../vs140/Creating-an-Extension-with-an-Editor-Item-Template.md)|  
|Visual Studio Package|Visual Basic and Visual C#<br /><br /> Extensibility<br /><br /> - or -<br /><br /> Other Project Types Extensibility|[Walkthrough: Creating a Menu Command with the Visual Studio Package Template](../vs140/Walkthrough--Creating-a-Menu-Command-By-Using-the-Visual-Studio-Package-Template.md)|  
|Visual Studio Shell Isolated|Other Project Types Extensibility|[Walkthrough: A Basic Isolated Shell Application](../vs140/Walkthrough--Creating-a-Basic-Isolated-Shell-Application.md)|  
  
## See Also  
 [VSPackages](../vs140/VSPackages.md)   
 [Visual Studio Shell (Isolated Mode)](../vs140/Visual-Studio-Isolated-Shell.md)   
 [Managed Extensibility Framework Overview](assetId:///6c61b4ec-c6df-4651-80f1-4854f8b14dde)   
 [The Visual Studio 2010 Editor](../Topic/Extending%20the%20Editor%20and%20Language%20Services.md)   
 [The Spectrum of Visual Studio Automation](assetId:///0382a061-d8bb-4732-b876-077244bb022f)