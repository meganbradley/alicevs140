---
title: "Changing List Control Styles"
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
ms.assetid: be74a005-0795-417c-9056-f6342aa74b26
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Changing List Control Styles
You can change the window style of a list control ([CListCtrl](../vs140/CListCtrl-Class.md)) at any time after you create it. By changing the window style, you change the kind of view the control uses. For example, to emulate the Explorer, you might supply menu items or toolbar buttons for switching the control between different views: icon view, list view, and so on.  
  
 For example, when the user selects your menu item, you could make a call to [GetWindowLong](http://msdn.microsoft.com/library/windows/desktop/ms633584) to retrieve the current style of the control and then call [SetWindowLong](http://msdn.microsoft.com/library/windows/desktop/ms633591) to reset the style. For more information, see [Using List View Controls](http://msdn.microsoft.com/library/windows/desktop/bb774736) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 Available styles are listed in [Create](../vs140/CListCtrl--Create.md). The styles `LVS_ICON`, `LVS_SMALLICON`, `LVS_LIST`, and `LVS_REPORT` designate the four list control views.  
  
## Extended Styles  
 In addition to the standard styles for a list control, there is another set, referred to as extended styles. These styles, discussed in [Extended List View Styles](http://msdn.microsoft.com/library/windows/desktop/bb774732) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)], provide a variety of useful features that customize the behavior of your list control. To implement the behavior of a certain style (such as hover selection), make a call to [CListCtrl::SetExtendedStyle](../vs140/CListCtrl--SetExtendedStyle.md), passing the needed style. The following example demonstrates the function call:  
  
 [!CODE [NVC_MFCControlLadenDialog#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#22)]  
  
> [!NOTE]
>  For hover selection to work, you must also have either **LVS_EX_ONECLICKACTIVATE** or **LVS_EX_TWOCLICKACTIVATE** turned on.  
  
## See Also  
 [Using CListCtrl](../vs140/Using-CListCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)