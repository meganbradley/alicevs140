---
title: "CMFCToolBarButton::HaveHotBorder"
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
ms.assetid: 169cd4c3-27da-40cf-83b7-b3b92eddfcd2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::HaveHotBorder
Determines whether a border of the button is displayed when a user selects the button.  
  
## Syntax  
  
```  
virtual BOOL HaveHotBorder() const;  
```  
  
## Return Value  
 This method returns `TRUE`.  
  
## Remarks  
 The framework calls this method to determine whether the toolbar button should display its border when a user selects it.  
  
 The default implementation returns `TRUE`. You can override this method to customize this behavior.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)