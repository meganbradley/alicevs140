---
title: "Enabling Tool Tips"
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
ms.assetid: 06b7c889-7722-4ce6-8b88-9efa50fe6369
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Enabling Tool Tips
You can enable tool tip support for the child controls of a window (such as the controls on a form view or dialog box).  
  
### To enable tool tips for the child controls of a window  
  
1.  Call `EnableToolTips` for the window for which you want to provide tool tips.  
  
2.  Provide a string for each control in your [TTN_NEEDTEXT notification](../vs140/Handling-TTN_NEEDTEXT-Notification-for-Tool-Tips.md) handler. The handler is in the message map of the window that contains the child controls (for example, your form view class). This handler should call a function that identifies the control and sets **pszText** to specify the text used by the tool tip control.  
  
## See Also  
 [Tool Tips in Windows Not Derived from CFrameWnd](../vs140/Tool-Tips-in-Windows-Not-Derived-from-CFrameWnd.md)