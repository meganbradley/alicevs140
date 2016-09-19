---
title: "Managing Application Resources (.NET)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f2582734-8ada-4baa-8a7c-e2ef943ddf7e
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Managing Application Resources (.NET)
Resource files are files that are part of an application but are not compiled, for example icon files or audio files. Since these files are not part of the compilation process, you can change them without having to recompile your binaries. If you are planning to localize your application, you should use resource files for all the strings and other resources that need to be changed when you localize your application.  
  
 For more information about resources in .NET desktop apps, see [Resources in Desktop Apps](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890). For more information about resources in C++ desktop apps, see [Working with Resource Files](../vs140/Working-with-Resource-Files.md).  
  
 Windows Store apps use a different resource model from desktop apps. For information about resources in Windows Store apps, see [Defining Application Resources](https://msdn.microsoft.com/en-us/library/windows/apps/hh465228.aspx) on the Windows Dev Center website.  
  
## Working with Resources  
 In a managed code project, open the project properties window (right-click the project node in **Solution Explorer** and select **Properties**, or type **project properties** in the **Quick Launch** window, or type ALT + ENTER in the **Solution Explorer** window). Select the **Resources** tab. You can add a .resx file if your project does not contain one already, add and delete different kinds of resources, and modify existing resources.  
  
 To find out how to work with resources in C++ projects, see [How to: Create a Resource](../vs140/How-to--Create-a-Resource.md).