---
title: "CMFCToolBar::IsButtonExtraSizeAvailable"
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
ms.assetid: d7cfb09e-c674-4fa7-a97e-21c5a5bd3888
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::IsButtonExtraSizeAvailable
Determines whether the toolbar can display buttons that have extended borders.  
  
## Syntax  
  
```  
virtual BOOL IsButtonExtraSizeAvailable() const;  
```  
  
## Return Value  
 `TRUE` if the bar can display buttons with the extra border size; otherwise `FALSE`.  
  
## Remarks  
 The toolbar object returns `TRUE` if it can display buttons that have extended borders. A toolbar button calls this method when it handles the [CMFCToolBarButton::OnChangeParentWnd](../vs140/CMFCToolBarButton--OnChangeParentWnd.md) notification and will set its internal extra border size flag accordingly. This internal flag may be retrieved later by calling [CMFCToolBarButton::IsExtraSize](../vs140/CMFCToolBarButton--IsExtraSize.md).  
  
 Override this method in a class derived from [CMFCToolBar](../Topic/CMFCToolBar%20Class.md) and return `TRUE` if your bar can display the toolbar buttons with the extra border size and return `FALSE` otherwise. The default implementation returns `TRUE`.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)