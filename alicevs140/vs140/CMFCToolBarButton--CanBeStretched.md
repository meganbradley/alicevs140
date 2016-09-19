---
title: "CMFCToolBarButton::CanBeStretched"
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
ms.assetid: ff931e47-cf05-4bfd-af60-d14508e5c05b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::CanBeStretched
Specifies whether a user can stretch the button during customization.  
  
## Syntax  
  
```  
virtual BOOL CanBeStretched() const;  
```  
  
## Return Value  
 This method returns `FALSE`.  
  
## Remarks  
 This method is used by the framework to determine whether the button can be stretched in customization mode.  
  
 The default implementation of this method returns `FALSE`. Override this method to return `TRUE` for a variable-width control such as a combo box or slider.  
  
 For more information about customization mode, see [CMFCToolBar::SetCustomizeMode](../vs140/CMFCToolBar--SetCustomizeMode.md).  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::SetCustomizeMode](../vs140/CMFCToolBar--SetCustomizeMode.md)