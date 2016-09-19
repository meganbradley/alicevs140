---
title: "CMFCToolBarButton::IsLocked"
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
ms.assetid: 95853fda-2ca2-496e-b216-2aa831d85173
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::IsLocked
Determines whether the button is on a locked (non-customizable) toolbar.  
  
## Syntax  
  
```  
BOOL IsLocked() const;  
```  
  
## Return Value  
 Nonzero if the button is on a locked toolbar; otherwise 0.  
  
## Remarks  
 The framework calls this method to determine whether the user can customize the toolbar button by using drag-and-drop or edit operations. Set the locked attribute on the parent toolbar by using the [CMFCToolBar::LoadToolBar](../vs140/CMFCToolBar--LoadToolBar.md) method. The framework passes the value of this attribute to the constructor of each toolbar button ([CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)) that it inserts into the parent toolbar.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::LoadToolBar](../vs140/CMFCToolBar--LoadToolBar.md)   
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)