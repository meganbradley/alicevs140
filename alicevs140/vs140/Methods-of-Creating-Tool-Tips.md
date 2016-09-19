---
title: "Methods of Creating Tool Tips"
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
ms.assetid: b015e9f4-ddfb-49a4-a5a6-fa2d45e4d328
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Methods of Creating Tool Tips
MFC provides three classes to create and manage the tool tip control: [CWnd](../vs140/CWnd-Class.md), [CToolBarCtrl](../vs140/CToolBarCtrl-Class.md), [CToolTipCtrl](../vs140/CToolTipCtrl-Class.md) and [CMFCToolTipCtrl](../vs140/CMFCToolTipCtrl-Class.md). The tool tip member functions in these classes wrap the Windows common control API. Class `CToolBarCtrl` and class `CToolTipCtrl` are derived from class `CWnd`.  
  
 `CWnd` provides four member functions to create and manage tool tips: [EnableToolTips](../vs140/CWnd--EnableToolTips.md), [CancelToolTips](../vs140/CWnd--CancelToolTips.md), [FilterToolTipMessage](../vs140/CWnd--FilterToolTipMessage.md), and [OnToolHitTest](../vs140/CWnd--OnToolHitTest.md). See these individual member functions for more information about how they implement tool tips.  
  
 If you create a toolbar using `CToolBarCtrl`, you can implement tool tips for that toolbar directly using the following member functions: [GetToolTips](../vs140/CToolBarCtrl--GetToolTips.md) and [SetToolTips](../vs140/CToolBarCtrl--SetToolTips.md). See these individual member functions and [Handling Tool Tip Notifications](../vs140/Handling-Tool-Tip-Notifications.md) for more information about how they implement tool tips.  
  
 The `CToolTipCtrl` class provides the functionality of the Windows common tool tip control. A single tool tip control can provide information for more than one tool. A tool is either a window, such as a child window or control, or an application-defined rectangular area within a window's client area. The [CMFCToolTipCtrl](../vs140/CMFCToolTipCtrl-Class.md) class derives from `CToolTipCtrl` and provides additional visual styles and functionality.  
  
## See Also  
 [Using CToolTipCtrl](../vs140/Using-CToolTipCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)