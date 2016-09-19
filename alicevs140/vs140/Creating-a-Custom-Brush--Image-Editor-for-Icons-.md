---
title: "Creating a Custom Brush (Image Editor for Icons)"
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
ms.assetid: 750881aa-6f47-4de9-8ca6-a7a12afc6383
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating a Custom Brush (Image Editor for Icons)
A custom brush is a rectangular portion of an image that you pick up and use like one of the Image editor's ready-made brushes. All operations you can perform on a selection, you can perform on a custom brush as well.  
  
### To create a custom brush from a portion of an image  
  
1.  [Select the part of the image](../vs140/Selecting-an-Area-of-an-Image--Image-Editor-for-Icons-.md) that you want to use for a brush.  
  
2.  Holding the **SHIFT** key down, click in the selection and drag it across the image.  
  
     \- or -  
  
3.  From the **Image** menu, choose **Use Selection as Brush**.  
  
     Your selection becomes a custom brush that distributes the colors in the selection across the image. Copies of the selection are left along the dragging path. The more slowly you drag, the more copies are made.  
  
     **Note** Clicking the **Use a Selection as Brush** without first selecting a portion of the image will use the whole image as a brush. The result of using a custom brush will also depend on whether you've selected an [Opaque or Transparent background](../vs140/Choosing-a-Transparent-or-Opaque-Background--Image-Editor-for-Icons-.md).  
  
 Pixels in a custom brush that match the current background color are normally transparent: they do not paint over the existing image. You can change this behavior so that background-color pixels paint over the existing image.  
  
 You can use the custom brush like a stamp or a stencil to create a variety of special effects.  
  
#### To draw custom brush shapes in the background color  
  
1.  [Select an opaque or transparent background](../vs140/Choosing-a-Transparent-or-Opaque-Background--Image-Editor-for-Icons-.md).  
  
2.  [Set the background color](../vs140/Selecting-Foreground-or-Background-Colors--Image-Editor-for-Icons-.md) to the color in which you want to draw.  
  
3.  Position the custom brush where you want to draw.  
  
4.  Click the right mouse button. Any opaque regions of the custom brush are drawn in the background color.  
  
#### To double or halve the custom brush size  
  
1.  Press the **PLUS SIGN** (**+**) key to double the brush size, or the **MINUS SIGN** (**–**) key to halve it.  
  
#### To cancel the custom brush  
  
1.  Press **ESC** or choose another drawing tool.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
### Requirements  
 None  
  
## See Also  
 [Accelerator Keys](../vs140/Accelerator-Keys--Image-Editor-for-Icons-.md)   
 [Editing Graphical Resources](../vs140/Editing-Graphical-Resources--Image-Editor-for-Icons-.md)   
 [Image Editor for Icons](../vs140/Image-Editor-for-Icons.md)