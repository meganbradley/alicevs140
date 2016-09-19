---
title: "Working with the Toolbar Control"
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
ms.assetid: b19409d5-3831-42c7-80ae-195c49dc9085
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Working with the Toolbar Control
This article explains how you can access the [CToolBarCtrl](../vs140/CToolBarCtrl-Class.md) object underlying a [CToolBar](../vs140/CToolBar-Class.md) for greater control over your toolbars. This is an advanced topic.  
  
## Procedures  
  
#### To access the toolbar common control underlying your CToolBar object  
  
1.  Call [CToolBar::GetToolBarCtrl](../vs140/CToolBar--GetToolBarCtrl.md).  
  
 `GetToolBarCtrl` returns a reference to a [CToolBarCtrl](../vs140/CToolBarCtrl-Class.md) object. You can use the reference to call member functions of the toolbar control class.  
  
> [!CAUTION]
>  While calling `CToolBarCtrl` **Get** functions is safe, use caution if you call the **Set** functions. This is an advanced topic. Normally you shouldn't need to access the underlying toolbar control.  
  
### What do you want to know more about?  
  
-   [Controls (Windows common controls)](../vs140/Controls--MFC-.md)  
  
-   [Toolbar fundamentals](../vs140/Toolbar-Fundamentals.md)  
  
-   [Docking and floating toolbars](../vs140/Docking-and-Floating-Toolbars.md)  
  
-   [Dynamically resizing the toolbar](../vs140/Docking-and-Floating-Toolbars.md)  
  
-   [Toolbar tool tips](../vs140/Toolbar-Tool-Tips.md)  
  
-   [Flyby status bar updates](../vs140/Toolbar-Tool-Tips.md)  
  
-   [Handling tool tip notifications](../vs140/Handling-Tool-Tip-Notifications.md)  
  
-   The [CToolBar](../vs140/CToolBar-Class.md) and [CToolBarCtrl](../vs140/CToolBarCtrl-Class.md) classes  
  
-   [Handling customization notifications](../vs140/Handling-Customization-Notifications.md)  
  
-   [Multiple toolbars](../vs140/Toolbar-Fundamentals.md)  
  
-   [Using your old toolbars](../vs140/Using-Your-Old-Toolbars.md)  
  
-   [Control bars](../vs140/Control-Bars.md)  
  
 For general information about using Windows common controls, see [Common Controls](http://msdn.microsoft.com/library/windows/desktop/bb775493).  
  
## See Also  
 [MFC Toolbar Implementation](../vs140/MFC-Toolbar-Implementation.md)