---
title: "CMFCToolBarButton::IsHidden"
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
ms.assetid: 138eef89-5be3-4fb4-9aca-d37b1ad59508
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::IsHidden
Determines whether the button is hidden.  
  
## Syntax  
  
```  
BOOL IsHidden() const;  
```  
  
## Return Value  
 Nonzero if the button is hidden (invisible); otherwise 0.  
  
## Remarks  
 The framework calls this method when the parent toolbar is stretched to determine whether the toolbar button is visible.  
  
 If you set the button to be invisible by using the [CMFCToolBarButton::SetVisible](../vs140/CMFCToolBarButton--SetVisible.md) method, use [CMFCToolBarButton::IsVisible](../vs140/CMFCToolBarButton--IsVisible.md) to determine whether the toolbar button is visible.  
  
 By default, all toolbar buttons are visible. Use the [CMFCToolBarButton::Show](../vs140/CMFCToolBarButton--Show.md) method to hide or show toolbar buttons.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::SetVisible](../vs140/CMFCToolBarButton--SetVisible.md)   
 [CMFCToolBarButton::IsVisible](../vs140/CMFCToolBarButton--IsVisible.md)   
 [CMFCToolBarButton::Show](../vs140/CMFCToolBarButton--Show.md)