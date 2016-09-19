---
title: "CMFCMenuButton::m_bStayPressed"
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
ms.assetid: 736b6ddd-0c97-4234-8bce-27e062678ab2
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuButton::m_bStayPressed
A Boolean member variable that indicates whether the menu button appears pressed while the user makes a selection from the pop-up menu.  
  
## Syntax  
  
```  
BOOL m_bStayPressed;  
```  
  
## Remarks  
 If the `m_bStayPressed` member is `FALSE`, the menu button does not become pressed when the uses clicks the button. In this case, the framework displays only the pop-up menu.  
  
 If the `m_bStayPressed` member is `TRUE`, the menu button becomes pressed when the user clicks the button. It stays pressed until after the user closes the pop-up menu, either by making a selection or canceling.  
  
## Requirements  
 **Header:** afxmenubutton.h  
  
## See Also  
 [CMFCMenuButton Class](../vs140/CMFCMenuButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)