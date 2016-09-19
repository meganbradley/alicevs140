---
title: "Creating a Device Image (Image Editor for Icons)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5a536928-32df-4ace-beb1-1521ce3b871f
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating a Device Image (Image Editor for Icons)
When you create a new icon or cursor resource, the Image editor first creates an image in a specific style (32 × 32, 16 colors for icons and 32 × 32, Monochrome for cursors). You can then add images in different sizes and styles to the initial icon or cursor and edit each additional image, as needed, for the different display devices. You can also edit an image by performing a cut-and-paste operation from an existing image type or from a bitmap created in a graphics program. For more information on the icon sizes that Windows uses, see [Icons](_win32_Icons_cpp) in the Windows SDK documentation.  
  
 When you open the icon or cursor resource in the [Image editor](../vs140/Image-Editor-for-Icons.md), the image most closely matching the current display device is opened by default.  
  
### To create a new icon or cursor  
  
1.  In [Resource View](../vs140/Resource-View-Window.md), right-click your .rc file, then choose **Insert Resource** from the shortcut menu. (If you already have an existing image resource in your .rc file, such as a cursor, you can simply right-click the **Cursor** folder and select **Insert Cursor** from the shortcut menu.)  
  
    > [!NOTE]
    >  If your project doesn't already contain an .rc file, please see [Creating a New Resource Script File](../vs140/How-to--Create-a-Resource-Script-File.md).  
  
2.  In the [Insert Resource dialog box](../vs140/Add-Resource-Dialog-Box.md), select **Icon** or **Cursor** and click **New**. For icons, this creates an icon resource with a 32 × 32, 16-color icon. For cursors, a 32 × 32, Monochrome (2-color) image is created.  
  
     If a plus sign (**+**) appears next to the image resource type in the **Insert Resource** dialog box, it means that toolbar templates are available. Click the plus sign to expand the list of templates, select a template, and click **New**.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
 **Requirements**  
  
 None  
  
## See Also  
 [Icons and Cursors: Image Resources for Display Devices](../vs140/Icons-and-Cursors--Image-Resources-for-Display-Devices--Image-Editor-for-Icons-.md)   
 [Accelerator Keys](../vs140/Accelerator-Keys--Image-Editor-for-Icons-.md)   
 [Icons and Cursors: Image Resources for Display Devices](../vs140/Icons-and-Cursors--Image-Resources-for-Display-Devices--Image-Editor-for-Icons-.md)