---
title: "CMFCMenuButton::m_bRightArrow"
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
ms.assetid: 7059e326-a3fc-4e2d-a5cf-041640c086c7
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuButton::m_bRightArrow
A Boolean member variable that indicates the location of the pop-up menu.  
  
## Syntax  
  
```  
BOOL m_bRightArrow;  
```  
  
## Remarks  
 When the user presses the menu button, the application shows a pop-up menu. The framework will display the pop-up menu either under the button or to the right of the button. The button also has a small arrow that indicates where the pop-up menu will appear. If `m_bRightArrow` is `TRUE`, the framework displays the pop-up menu to the right of the button. Otherwise, it displays the pop-up menu under the button.  
  
## Requirements  
 **Header:** afxmenubutton.h  
  
## See Also  
 [CMFCMenuButton Class](../vs140/CMFCMenuButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)