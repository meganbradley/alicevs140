---
title: "Icons and Cursors: Image Resources for Display Devices (Image Editor for Icons)"
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
ms.assetid: 8f0809a8-0cf0-4da9-b23d-51f28bf15f5b
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Icons and Cursors: Image Resources for Display Devices (Image Editor for Icons)
Icons and cursors are graphical resources that can contain multiple images in different sizes and color schemes for different types of display devices. In addition, a cursor has a "hot spot," the location Windows uses to track its position. Both icons and cursors are created and edited using the Image editor, as are bitmaps and other images.  
  
 When you create a new icon or cursor, the Image editor first creates an image of a standard type. The image is initially filled with the screen (transparent) color. If the image is a cursor, the hot spot is initially the upper-left corner (coordinates 0,0).  
  
 By default, the Image editor supports the creation of additional images for the devices shown in the following table. You can create images for other devices by typing width, height, and color-count parameters into the [Custom Image dialog box](../vs140/Custom-Image-Dialog-Box--Image-Editor-for-Icons-.md).  
  
> [!NOTE]
>  Using the Image Editor, you can view 32-bit images, but you cannot edit them.  
  
|Color|Width (pixels)|Height (pixels)|  
|-----------|----------------------|-----------------------|  
|Monochrome|16|16|  
|Monochrome|32|32|  
|Monochrome|48|48|  
|Monochrome|64|64|  
|Monochrome|96|96|  
|16|16|16|  
|16|32|32|  
|16|64|64|  
|16|48|48|  
|16|96|96|  
|256|16|16|  
|256|32|32|  
|256|48|48|  
|256|64|64|  
|256|96|96|  
  
-   [Creating a New Device Image (Icon or Cursor)](../vs140/Creating-a-Device-Image--Image-Editor-for-Icons-.md)  
  
-   [Adding an Image for a Different Display Device](../vs140/Adding-an-Image-for-a-Different-Display-Device--Image-Editor-for-Icons-.md)  
  
-   [Copying a Device Image](../vs140/Copying-a-Device-Image--Image-Editor-for-Icons-.md)  
  
-   [Deleting a Device Image](../vs140/Deleting-a-Device-Image--Image-Editor-for-Icons-.md)  
  
-   [Creating Transparent or Inverse Regions in Device Images](../vs140/Creating-Transparent-or-Inverse-Regions-in-Device-Images--Image-Editor-for-Icons-.md)  
  
-   [Creating a 256-Color Icon or Cursor](../vs140/Creating-a-256-Color-Icon-or-Cursor--Image-Editor-for-Icons-.md)  
  
-   [Setting a Cursor's Hot Spot](../vs140/Setting-a-Cursor-s-Hot-Spot--Image-Editor-for-Icons-.md)  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
## Requirements  
 None  
  
## See Also  
 [Image Editor for Icons](../vs140/Image-Editor-for-Icons.md)   
 [Icons](http://msdn.microsoft.com/library/windows/desktop/ms646973)   
 [Cursors](http://msdn.microsoft.com/library/windows/desktop/ms646970)