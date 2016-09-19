---
title: "Converting Bitmaps to Toolbars"
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
ms.assetid: 971c181b-40f5-44be-843d-677a7c235667
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Converting Bitmaps to Toolbars
You can create a new toolbar by converting a bitmap. The graphic from the bitmap converts to the button images for a toolbar. Usually the bitmap contains several button images on a single bitmap, with one image for each button. Images can be any size; the default is 16 pixels wide and the height of the image. You can specify the size of the button images in the [New Toolbar Resource dialog box](../vs140/New-Toolbar-Resource-Dialog-Box.md) when you choose Toolbar Editor from the **Image** menu while in the Image editor.  
  
### To convert bitmaps to a toolbar  
  
1.  Open an existing bitmap resource in the [Image editor](../vs140/Image-Editor-for-Icons.md). (If the bitmap is not already in your .rc file, right-click the .rc file, choose **Import** from the shortcut menu, navigate to the bitmap you want to add to your .rc file, then click **Open**.)  
  
2.  From the **Image** menu, choose **Toolbar Editor**.  
  
     The [New Toolbar Resource dialog box](../vs140/New-Toolbar-Resource-Dialog-Box.md) appears. You can change the width and height of the icon images to match the bitmap. The toolbar image is then displayed in the Toolbar editor.  
  
3.  To finish the conversion, change the command **ID** of the button using the [Properties window](../vs140/Properties-Window.md). Type the new **ID** or select an **ID** from the drop-down list.  
  
    > [!TIP]
    >  The Properties window contains a pushpin button in the title bar. Clicking this button enables or disables Auto Hide for the window. To quickly cycle through all the toolbar button properties without having to reopen the individual property windows, turn Auto Hide off so the Properties window stays stationary.  
  
 You can also change the command IDs of the buttons on the new toolbar by using the [Properties window](../vs140/Properties-Window.md). For information on editing the new toolbar, see [Creating, Moving, and Editing Toolbar Buttons](../vs140/Creating--Moving--and-Editing-Toolbar-Buttons.md).  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
 Requirements  
  
 MFC or ATL  
  
## See Also  
 [Creating New Toolbars](../vs140/Creating-New-Toolbars.md)   
 [Toolbar Editor](../vs140/Toolbar-Editor.md)