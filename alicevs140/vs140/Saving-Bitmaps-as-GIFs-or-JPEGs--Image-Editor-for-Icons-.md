---
title: "Saving Bitmaps as GIFs or JPEGs (Image Editor for Icons)"
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
ms.assetid: 115df69f-10fb-4e6f-906b-853c1e4a54af
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Saving Bitmaps as GIFs or JPEGs (Image Editor for Icons)
When you create a bitmap, the image is created in bitmap format (.bmp). You can, however, save the image as a GIF or JPEG or in other graphic formats.  
  
> [!NOTE]
>  This process does not apply to icons and cursors.  
  
### To create and save a bitmap as a .gif or .jpeg  
  
1.  From the **File** menu, choose **Open**, then click **File**.  
  
2.  In the **New File dialog box**, click the **Visual C++** folder, then select **Bitmap File (.bmp)** in the **Templates** box and click **Open**.  
  
     The bitmap opens in the **Image** editor.  
  
3.  Make changes to your new bitmap as needed.  
  
4.  With the bitmap still open in the **Image** editor, click **Save *filename*.bmp As** on the **File** menu.  
  
5.  In the **Save File As** dialog box, type the name you want to give the file and the extension that denotes the file format you want in the **File Name** box. For example, myfile.gif.  
  
     **Note**  You must create or open the bitmap outside of your project in order to save it as another file format. If you create or open it within your project, the **Save As** command will be unavailable. For more information, see [Viewing Resources in a Resource Script File Outside of a Project (Standalone)](../vs140/How-to--Open-a-Resource-Script-File-Outside-of-a-Project--Standalone-.md).  
  
6.  Click **Save**.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
## See Also  
 [Editing Graphical Resources](../vs140/Editing-Graphical-Resources--Image-Editor-for-Icons-.md)   
 [Image Editor for Icons](../vs140/Image-Editor-for-Icons.md)