---
title: "Aligning Controls on a Guide"
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
ms.assetid: 17db84ba-5288-4478-be57-afa748aa6447
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Aligning Controls on a Guide
The sizing handles of controls snap to guides when the controls are moved, and guides snap to controls (if there are no controls previously snapped to the guide). When a guide is moved, controls that are snapped to it move as well. Controls snapped to more than one guide are resized when one of the guides is moved.  
  
 The tick marks in the rulers that determine the spacing of guides and controls are defined by dialog units (DLUs). A DLU is based on the size of the dialog box font, normally 8-point MS Shell Dlg. A horizontal DLU is the average width of the dialog box font divided by four. A vertical DLU is the average height of the font divided by eight.  
  
### To size a group of controls with guides  
  
1.  Snap one side of the control (or controls) to a guide.  
  
2.  Drag a guide to the other side of the control (or controls).  
  
     If necessary with multiple controls, size each to snap to the second guide.  
  
3.  Move either guide to size the control (or controls).  
  
### To change the intervals of the tick marks  
  
1.  From the **Format** menu, choose **Guide Settings**.  
  
2.  In the [Guide Settings Dialog Box](../vs140/Guide-Settings-Dialog-Box.md), in the **Grid Spacing** field, specify a new width and height in DLUs.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
 Requirements  
  
 Win32  
  
## See Also  
 [Dialog Editor States (Guides and Grids)](../vs140/Dialog-Editor-States--Guides-and-Grids-.md)   
 [Controls in Dialog Boxes](../vs140/Controls-in-Dialog-Boxes.md)