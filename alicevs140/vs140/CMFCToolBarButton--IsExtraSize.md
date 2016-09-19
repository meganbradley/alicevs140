---
title: "CMFCToolBarButton::IsExtraSize"
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
ms.assetid: 33fd99cb-921d-458d-bd53-2f21072f41c8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::IsExtraSize
Determines whether the button can be displayed with an extended border.  
  
## Syntax  
  
```  
virtual BOOL IsExtraSize() const;  
```  
  
## Return Value  
 Nonzero if the toolbar button can be displayed with an extended border; otherwise 0.  
  
## Remarks  
 Several skins use extra size for the borders of toolbar buttons (for example, round buttons).  
  
 If the user moves this button from one toolbar to another, the framework calls the [CMFCToolBarButton::OnChangeParentWnd](../vs140/CMFCToolBarButton--OnChangeParentWnd.md) method. The [CMFCToolBarButton::OnChangeParentWnd](../vs140/CMFCToolBarButton--OnChangeParentWnd.md) method sets the extra size flag to that of the new parent toolbar (for more information, see [CMFCToolBar::IsButtonExtraSizeAvailable](../vs140/CMFCToolBar--IsButtonExtraSizeAvailable.md)).  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::OnChangeParentWnd](../vs140/CMFCToolBarButton--OnChangeParentWnd.md)   
 [CMFCToolBar::IsButtonExtraSizeAvailable](../vs140/CMFCToolBar--IsButtonExtraSizeAvailable.md)