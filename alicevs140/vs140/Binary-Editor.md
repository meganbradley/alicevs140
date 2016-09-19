---
title: "Binary Editor"
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
ms.assetid: 2483c48b-1252-4dbc-826b-82e6c1a0e9cb
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Binary Editor
> [!WARNING]
>  The Binary Editor is not available in Express editions.  
  
 The Binary editor allows you to edit any resource at the binary level in either hexadecimal or ASCII format. You can also use the [Find command](../vs140/Find-Command.md) to search for either ASCII strings or hexadecimal bytes. You should use the Binary editor only when you need to view or make minor changes to custom resources or resource types not supported by the Visual Studio environment.  
  
 To open the Binary Editor, first choose **File &#124; New &#124; File** from the main menu, select the file you want to edit, then click on the drop arrow next to the **Open** button, and choose **Open With &#124; Binary Editor**.  
  
> [!CAUTION]
>  Editing resources such as dialog boxes, images, or menus in the Binary editor is dangerous. Incorrect editing could corrupt the resource, making it unreadable in its native editor.  
  
> [!TIP]
>  While using the Binary editor, in many instances, you can right-click to display a shortcut menu of resource-specific commands. The commands available depend on what your cursor is pointing to. For example, if you click while pointing to the Binary editor with selected hexadecimal values, the shortcut menu shows the **Cut**, **Copy**, and **Paste** commands.  
  
 With the Binary editor, you can:  
  
-   [Open a resource for binary editing](../vs140/Opening-a-Resource-for-Binary-Editing.md)  
  
-   [Edit binary data](../vs140/Editing-Binary-Data.md)  
  
-   [Find binary data](../vs140/Finding-Binary-Data.md)  
  
-   [Create a new custom or data resource](../vs140/Creating-a-New-Custom-or-Data-Resource.md)  
  
## Managed Resources  
 You can use the [Image editor](../vs140/Image-Editor-for-Icons.md) and the Binary editor to work with resource files in managed projects. Any managed resources you want to edit must be linked resources. The Visual Studio resource editors do not support editing embedded resources.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
### Requirements  
 None  
  
## See Also  
 [Resource Editors](../vs140/Resource-Editors.md)