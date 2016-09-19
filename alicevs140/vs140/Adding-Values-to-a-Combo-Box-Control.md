---
title: "Adding Values to a Combo Box Control"
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
ms.assetid: 22a78f98-fada-48b3-90d8-7fa0d8e4de51
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Adding Values to a Combo Box Control
You can add values to a combo box control as long as you have the Dialog editor open.  
  
> [!TIP]
>  It's a good idea to add all values to the combo box *before* you size the box in the Dialog editor, or you may truncate text that should appear in the combo control.  
  
#### To enter values into a combo box control  
  
1.  Select the combo box control by clicking on it.  
  
2.  In the [Properties Window](../vs140/Properties-Window.md), scroll down to the **Data** property.  
  
    > [!NOTE]
    >  If you are displaying properties grouped by type, **Data** appears in the **Misc** properties.  
  
3.  Click in the value area for the **Data** property and type in your data values, separated by semicolons.  
  
    > [!NOTE]
    >  Do not put spaces between values because spaces interfere with alphabetizing in the drop-down list.  
  
4.  Click **Enter** when you are finished adding values.  
  
 For information on enlarging the drop-down portion of a combo box, see [Setting the Size of the Combo Box and Its Drop-Down List](../vs140/Setting-the-Size-of-the-Combo-Box-and-Its-Drop-Down-List.md).  
  
> [!NOTE]
>  You cannot add values to Win32 projects using this procedure (the **Data** property is grayed out for Win32 projects). Because Win32 projects do not have libraries that add this capability, you must add values to a combo box with a Win32 project programmatically.  
  
#### To test the appearance of values in a combo box  
  
1.  After entering values in the **Data** property, click the **Test** button on the [Dialog Editor Toolbar](../vs140/Showing-or-Hiding-the-Dialog-Editor-Toolbar.md).  
  
     Try scrolling down the entire value list. Values appear exactly as they are typed in the **Data** property in the Properties window. There is no spelling or capitalization checking.  
  
     Press ESC to return to the Dialog box editor.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
### Requirements  
 Win32  
  
## See Also  
 [Controls in Dialog Boxes](../vs140/Controls-in-Dialog-Boxes.md)   
 [Controls](../vs140/Controls--MFC-.md)