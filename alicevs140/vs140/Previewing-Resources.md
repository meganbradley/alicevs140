---
title: "Previewing Resources"
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
ms.assetid: d6abda66-0e2b-4ac3-a59a-a57b8c6fb70b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Previewing Resources
Previewing your resources allows you to view graphical resource without opening them. Previewing is also useful for executables after you've compiled them because the resource identifiers change to numbers. Since these numeric identifiers often don't provide enough information, previewing the resources helps you quickly identify them.  
  
 You can preview the visual layout of the following resource types:  
  
-   Bitmap  
  
-   Dialog  
  
-   Icon  
  
-   Menu  
  
-   Cursor  
  
-   Toolbar  
  
 The visual preview function does not apply to Accelerator, Manifest, String Table, and Version Information resources.  
  
### To preview resources  
  
1.  In [Resource View](../vs140/Resource-View-Window.md) or a document window, select your resource, for example, IDD_ABOUTBOX.  
  
     **Note** If your project doesn't already contain an .rc file, please see [Creating a New Resource Script File](../vs140/How-to--Create-a-Resource-Script-File.md).  
  
2.  In the [Properties window](../vs140/Properties-Window.md), click the **Property Pages** button.  
  
     \- or -  
  
3.  On the **View** menu, click **Property Pages**.  
  
     The Property Page for the resource opens displaying a preview of that resource. You can then use the Up and Down arrow keys to navigate the tree control in Resource View or the document window. The Property Page will stay open and show any resource that has focus and is able to be previewed.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
 **Requirements**  
  
 Win32  
  
## See Also  
 [How to: Open a Resource Script File Outside of a Project (Standalone)](../vs140/How-to--Open-a-Resource-Script-File-Outside-of-a-Project--Standalone-.md)   
 [Resource Editors](../vs140/Resource-Editors.md)