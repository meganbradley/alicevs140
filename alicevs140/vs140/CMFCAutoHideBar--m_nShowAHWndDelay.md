---
title: "CMFCAutoHideBar::m_nShowAHWndDelay"
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
ms.topic: reference
ms.assetid: 2707353d-ce25-4ea3-a611-13d52cb56ab0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCAutoHideBar::m_nShowAHWndDelay
The time delay between the moment when the user places the mouse cursor over a [CMFCAutoHideButton Class](../vs140/CMFCAutoHideButton-Class.md) and the moment when the framework shows the associated window.  
  
## Syntax  
  
```  
int CMFCAutoHideBar::m_nShowAHWndDelay = 400;  
```  
  
## Remarks  
 When the user places the mouse cursor over a `CMFCAutoHideButton`, there is a slight delay before the framework displays the associated window. This parameter determines the length of that delay in milliseconds.  
  
## Requirements  
 **Header:** afxautohidebar.h  
  
## See Also  
 [CMFCAutoHideBar Class](../vs140/CMFCAutoHideBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCAutoHideButton Class](../vs140/CMFCAutoHideButton-Class.md)