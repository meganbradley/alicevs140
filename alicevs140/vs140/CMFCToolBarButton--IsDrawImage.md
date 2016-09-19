---
title: "CMFCToolBarButton::IsDrawImage"
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
ms.assetid: 670d3ad8-66b7-40bf-9761-ea641c907c58
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::IsDrawImage
Determines whether an image is displayed on the button.  
  
## Syntax  
  
```  
BOOL IsDrawImage() const;  
```  
  
## Return Value  
 Nonzero if an image is displayed on the button; otherwise 0.  
  
## Remarks  
 This method returns `FALSE` if the toolbar button has no associated image ([CMFCToolBarButton::GetImage](../vs140/CMFCToolBarButton--GetImage.md) returns -1) or if [CMFCToolBarButton::m_bImage](../vs140/CMFCToolBarButton--m_bImage.md) is set to `FALSE`.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::GetImage](../vs140/CMFCToolBarButton--GetImage.md)   
 [CMFCToolBarButton::m_bImage](../vs140/CMFCToolBarButton--m_bImage.md)