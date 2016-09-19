---
title: "Viewing and Editing Resources in a Resource Editor"
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
ms.assetid: ba8bdc07-3f60-43c7-aa5c-d5dd11f0966e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Viewing and Editing Resources in a Resource Editor
Each resource type has a Resource editor specific to that resource type. You can rearrange, resize, add controls and features, or otherwise modify aspects of a resource using the associated editor. You can also edit a resource in [text format](../vs140/How-to--Open-a-Resource-Script-File-in-Text-Format.md) and [binary format](../vs140/Opening-a-Resource-for-Binary-Editing.md).  
  
 Some resource types are individual files that can be imported and used in various ways; these include bitmaps, icons, cursors, toolbars, and html files. Such resources have file names as well as [resource identifiers](../vs140/Symbols--Resource-Identifiers.md). Others, such as dialogs, menus, and string tables in Win32 projects, exist only as part of a resource script (.rc) file or resource template (.rct) file.  
  
> [!NOTE]
>  Properties of a resource [can be modified using the Properties window](../vs140/Changing-the-Properties-of-a-Resource.md).  
  
## Win32 Resources  
 You can access Win32 resources in the [Resource View](../vs140/Resource-View-Window.md) pane.  
  
#### To view a Win32 resource in a resource editor  
  
1.  Select **Resource View** from the **View** menu.  
  
2.  If the Resource View window is not the top-most window, click the **Resource View** tab to bring it to the top.  
  
3.  From Resource View, expand the folder for the project that contains resources you want to view. For example, if you want to view a dialog resource, expand the Dialog folder.  
  
    > [!NOTE]
    >  If your project doesn't already contain an .rc file, please see [Creating a New Resource Script File](../vs140/How-to--Create-a-Resource-Script-File.md).  
  
4.  Double-click the resource, for example, IDD_ABOUTBOX.  
  
     The resource opens in the appropriate editor. For example, for dialog resources, the resource opens inside the Dialog editor.  
  
     You can also [view resources in an .rc (resource script) file without having a project open](../vs140/How-to--Open-a-Resource-Script-File-Outside-of-a-Project--Standalone-.md).  
  
#### To delete an existing Win 32 resource  
  
1.  In Resource View, expand the node for a resource type.  
  
2.  Right-click on the resource you want to delete and choose **Delete** from the shortcut menu.  
  
    > [!NOTE]
    >  You can delete a resource using the same shortcut menu command when you have the .rc file open in a document window outside a project.  
  
## Resources in Managed Projects  
 Because managed projects do not use resource script files, you must open your resources from **Solution Explorer**. You can use the [Image editor](../vs140/Image-Editor-for-Icons.md) and the [Binary editor](../vs140/Binary-Editor.md) to work with resource files in managed projects. Any managed resources you want to edit must be linked resources. The Visual Studio resource editors do not support editing embedded resources.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
#### To view a managed resource in a resource editor  
  
1.  In Solution Explorer, double-click the resource, for example, Bitmap1.bmp.  
  
     The resource opens in the appropriate editor.  
  
#### To delete an existing managed resource  
  
1.  In Solution Explorer, right-click the resource you want to delete and choose **Delete** from the shortcut menu.  
  
### Requirements  
 None  
  
## See Also  
 [Resource Editors](../vs140/Resource-Editors.md)