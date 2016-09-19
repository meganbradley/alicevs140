---
title: "CMFCMenuButton::m_bOSMenu"
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
ms.assetid: 2183385c-df94-46a2-a7df-8673a78a9ed9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuButton::m_bOSMenu
A Boolean member variable that indicates which pop-up menu the framework displays.  
  
## Syntax  
  
```  
BOOL m_bOSMenu;  
```  
  
## Remarks  
 If `m_bOSMenu` is `TRUE`, the framework calls the inherited `TrackPopupMenu` method for this object. Otherwise, the framework calls [CContextMenuManager::TrackPopupMenu](../vs140/CContextMenuManager--TrackPopupMenu.md).  
  
## Requirements  
 **Header:** afxmenubutton.h  
  
## See Also  
 [CMFCMenuButton Class](../vs140/CMFCMenuButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)