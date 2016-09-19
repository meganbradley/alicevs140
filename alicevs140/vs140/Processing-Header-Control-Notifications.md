---
title: "Processing Header-Control Notifications"
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
ms.assetid: e6c6af7c-d458-4d33-85aa-48014ccde5f6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Processing Header-Control Notifications
In your view or dialog class, use the Properties window to create an [OnChildNotify](../vs140/CWnd--OnChildNotify.md) handler function with a switch statement for any header-control ([CHeaderCtrl](../vs140/CHeaderCtrl-Class.md)) notification messages you want to handle (see [Mapping Messages to Functions](../vs140/Mapping-Messages-to-Functions.md)). Notifications are sent to the parent window when the user clicks or double-clicks a header item, drags a divider between items, and so on.  
  
 The notification messages associated with a header control are listed in [Header Control Reference](http://msdn.microsoft.com/library/windows/desktop/bb775239) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [Using CHeaderCtrl](../vs140/Using-CHeaderCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)