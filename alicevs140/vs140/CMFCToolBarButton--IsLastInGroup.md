---
title: "CMFCToolBarButton::IsLastInGroup"
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
ms.assetid: b5ec711d-ad2a-4bf7-be73-106e1216956a
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::IsLastInGroup
Specifies whether the button is in the last position in its button group.  
  
## Syntax  
  
```  
virtual BOOL IsLastInGroup() const;  
```  
  
## Return Value  
 `TRUE` if the button is the last button in its button group; otherwise `FALSE`.  
  
## Remarks  
 This method defines a *button group* as a neighboring set of buttons that are positioned on the same row and are bounded by separators or the border of the toolbar This method returns `FALSE` if the toolbar button has no parent toolbar or the toolbar button refers to the **Customize** button. For more information about the **Customize** button, see [CMFCToolBar::GetCustomizeButton](../vs140/CMFCToolBar--GetCustomizeButton.md).  
  
 Call the [CMFCToolBarButton::IsFirstInGroup](../vs140/CMFCToolBarButton--IsFirstInGroup.md) method to determine whether the button is in the first position in its button group.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::GetCustomizeButton](../vs140/CMFCToolBar--GetCustomizeButton.md)   
 [CMFCToolBarButton::IsFirstInGroup](../vs140/CMFCToolBarButton--IsFirstInGroup.md)