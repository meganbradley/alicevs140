---
title: "Changing the Tab Order of Controls"
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
ms.assetid: e2cee764-4367-42d7-9563-65a68f76f5ff
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Changing the Tab Order of Controls
The tab order is the order in which the TAB key moves the input focus from one control to the next within a dialog box. Usually the tab order proceeds from left to right and from top to bottom in a dialog box. Each control has a **Tabstop** property that determines whether a control receives input focus.  
  
### To set input focus for a control  
  
1.  In the [Properties Window](../vs140/Properties-Window.md), select **True** or **False** in the **Tabstop** property.  
  
 Even controls that do not have the Tabstop property set to True need to be part of the tab order. This can be important, for example, when you [define access keys (mnemonics)](../vs140/Defining-Mnemonics--Access-Keys-.md) for controls that do not have captions. Static text that contains an access key for a related control must immediately precede the related control in the tab order.  
  
> [!NOTE]
>  If your dialog box contains overlapping controls, changing the tab order may change the way the controls are displayed. Controls that come later in the tab order are always displayed on top of any overlapping controls that precede them in the tab order.  
  
#### To view the current tab order for all controls in a dialog box  
  
1.  On the **Format** menu, click **Tab Order**.  
  
 \- or -  
  
-   Press CTRL + D.  
  
#### To change the tab order for all controls in a dialog box  
  
1.  On the **Format** menu, click **Tab Order**.  
  
     A number in the upper-left corner of each control shows its place in the current tab order.  
  
2.  Set the tab order by clicking each control in the order you want the TAB key to follow.  
  
3.  Press **ENTER** to exit **Tab Order** mode.  
  
    > [!TIP]
    >  Once you enter Tab Order mode, you can press ESC or ENTER to disable the ability to change the tab order.  
  
#### To change the tab order for two or more controls  
  
1.  From the **Format** menu, choose **Tab Order**.  
  
2.  Specify where the change in order will begin. To do this, hold down the **CTRL** key and click the control prior to the one where you want the changed order to begin.  
  
     For example, if you want to change the order of controls 7 through 9, hold down CTRL, then select control 6 first.  
  
    > [!NOTE]
    >  To set a specific control to number 1 (first in the tab order), double-click the control.  
  
3.  Release the CTRL key, then click the controls in the order you want the TAB key to follow from that point.  
  
4.  Press **ENTER** to exit **Tab Order** mode.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
### Requirements  
 Win32  
  
## See Also  
 [Arrangement of Controls on Dialog Boxes](../vs140/Arrangement-of-Controls-on-Dialog-Boxes.md)   
 [Controls in Dialog Boxes](../vs140/Controls-in-Dialog-Boxes.md)   
 [Controls](../vs140/Controls--MFC-.md)