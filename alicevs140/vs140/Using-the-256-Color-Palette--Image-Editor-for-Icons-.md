---
title: "Using the 256-Color Palette (Image Editor for Icons)"
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
ms.assetid: 1506ed00-669b-4a21-b1a4-39b6a84a78bb
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using the 256-Color Palette (Image Editor for Icons)
To draw with a selection from the 256-color palette, you need to select the colors from the Colors palette in the [Colors window](../vs140/Colors-Window--Image-Editor-for-Icons-.md).  
  
### To choose a color from the 256-color palette for large icons  
  
1.  Select the large icon or cursor, or create a new large icon or cursor.  
  
2.  Choose a color from the 256 colors displayed in the **Colors** palette in the **Colors** window.  
  
     The color selected will become the current color in the colors palette in the **Colors** window.  
  
    > [!NOTE]
    >  The initial palette used for 256-color images matches the palette returned by the CreateHalftonePalette Windows API. All icons intended for the Windows shell should use this palette to prevent flicker during palette realization.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
 Requirements  
  
 None  
  
## See Also  
 [Accelerator Keys](../vs140/Accelerator-Keys--Image-Editor-for-Icons-.md)   
 [Creating a 256-Color Icon or Cursor](../vs140/Creating-a-256-Color-Icon-or-Cursor--Image-Editor-for-Icons-.md)   
 [Icons and Cursors: Image Resources for Display Devices](../vs140/Icons-and-Cursors--Image-Resources-for-Display-Devices--Image-Editor-for-Icons-.md)