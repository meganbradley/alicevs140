---
title: "Working with Color (Image Editor for Icons)"
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
ms.assetid: d34ff96f-241d-494f-abdd-13811ada8cd3
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Working with Color (Image Editor for Icons)
The Image editor contains many features that specifically handle and customize colors. You can set a foreground or background color, fill bounded areas with color, or select a color on an image to use as the current foreground or background color. You can use tools on the [Image Editor toolbar](../vs140/Toolbar--Image-Editor-for-Icons-.md) along with the colors palette in the [Colors window](../vs140/Colors-Window--Image-Editor-for-Icons-.md) to create images.  
  
 All colors for monochrome and 16-color images are shown in the Colors palette in the Colors window. In addition to the 16 standard colors, you can create your own custom colors. Changing any of the colors in the palette will immediately change the corresponding color in the image.  
  
 When working with 256-color icon and cursor images, the Colors property in the [Properties window](../vs140/Properties-Window.md) is used. For more information, see [Creating a 256-color icon or cursor](../vs140/Creating-a-256-Color-Icon-or-Cursor--Image-Editor-for-Icons-.md).  
  
> [!NOTE]
>  Using the Image Editor, you can view 32-bit images, but you cannot edit them.  
  
 True-color images can also be created. However, true color samples do not appear in the full palette in the Colors window; they appear only in the foreground or background color indicator area. True colors are created using the [Custom Color Selector dialog box](../vs140/Custom-Color-Selector-Dialog-Box--Image-Editor-for-Icons-.md). For more information, see [Customizing or changing colors](../vs140/Customizing-or-Changing-Colors--Image-Editor-for-Icons-.md).  
  
 You can save customized color palettes on disk and reload them as needed. The color palette you used most recently is saved in the Registry and automatically loaded the next time you start Visual Studio.  
  
-   [Selecting Foreground or Background Colors](../vs140/Selecting-Foreground-or-Background-Colors--Image-Editor-for-Icons-.md)  
  
-   [Filling a Bounded Area of an Image with a Color](../vs140/Filling-a-Bounded-Area-of-an-Image-with-a-Color--Image-Editor-for-Icons-.md)  
  
-   [Picking up a Color from an Image to Use Elsewhere](../vs140/Picking-up-a-Color-from-an-Image-to-Use-Elsewhere--Image-Editor-for-Icons-.md)  
  
-   [Choosing a Transparent or Opaque Background](../vs140/Choosing-a-Transparent-or-Opaque-Background--Image-Editor-for-Icons-.md)  
  
-   [Inverting the Colors in a Selection](../vs140/Inverting-the-Colors-in-a-Selection--Image-Editor-for-Icons-.md)  
  
-   [Customizing or Changing Colors](../vs140/Customizing-or-Changing-Colors--Image-Editor-for-Icons-.md)  
  
-   [Saving and Loading Different Color Palettes](../vs140/Saving-and-Loading-Different-Color-Palettes--Image-Editor-for-Icons-.md)  
  
-   [Colors Window](../vs140/Colors-Window--Image-Editor-for-Icons-.md)  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
## Requirements  
 None  
  
## See Also  
 [Accelerator Keys](../vs140/Accelerator-Keys--Image-Editor-for-Icons-.md)   
 [Resources](_win32_Resources)