---
title: "Introducing the Visual Studio SDK"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a308a6ce-d2da-47be-81ef-5b44169f2882
caps.latest.revision: 198
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Introducing the Visual Studio SDK
The Visual Studio SDK is a set of tools and documentation that can help you extend Visual Studio or create new features that are integrated into Visual Studio. You can distribute your extensions to other users. The following are some of the ways in which you can extend Visual Studio:  
  
-   Add commands, windows, and other features to the IDE.  
  
-   Extend the Visual Studio editor.  
  
-   Enable support for a new language.  
  
-   Add a custom project type.  
  
## Using VSPackages and the Managed Extensibility Framework to Extend Visual Studio  
 Many Visual Studio components are software modules called VSPackages, including windows, services, and project types. By creating your own VSPackages, you can add features to Visual Studio for your own use or for distribution to other users.  
  
 The Visual Studio editor is composed of a VSPackage plus a number of Managed Extensibility Framework (MEF) extensions. You can use MEF extensions to extend and customize the Visual Studio editor.  
  
 The Visual Studio SDK includes tools and documentation to help you create VSPackages and MEF extensions. You can use [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)], [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)], or [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] to write your extensions.  
  
 For more information, see  
  
-   [Getting Started with the Visual Studio Integration SDK](../vs140/Starting-to-Develop-Visual-Studio-Extensions.md)  
  
-   [Developing Visual Studio Extensions](../vs140/Developing-Visual-Studio-Extensions.md)  
  
## See Also  
 [The Visual Studio SDK](../vs140/Visual-Studio-SDK.md)