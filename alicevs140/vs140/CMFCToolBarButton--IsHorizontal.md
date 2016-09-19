---
title: "CMFCToolBarButton::IsHorizontal"
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
ms.assetid: 207fc986-a245-483c-a763-6d8741724171
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::IsHorizontal
Determines whether the button is located on a horizontal toolbar.  
  
## Syntax  
  
```  
BOOL IsHorizontal() const;  
```  
  
## Return Value  
 Nonzero if a toolbar button is located on a horizontal toolbar; otherwise 0.  
  
## Remarks  
 The framework calls this method to determine the layout of toolbar buttons.  
  
 This method returns the `m_bHorz` data member. The default value of the `m_bHorz` data member is `TRUE`; it is reset on each call to the [CMFCToolBarButton::OnDraw](../vs140/CMFCToolBarButton--OnDraw.md) method.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::OnDraw](../vs140/CMFCToolBarButton--OnDraw.md)