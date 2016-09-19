---
title: "CMFCToolBarButton::IsDrawText"
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
ms.assetid: 5ec5d9b1-9313-4788-996d-0a8e55a59b46
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::IsDrawText
Determines whether a text label is displayed on the button.  
  
## Syntax  
  
```  
BOOL IsDrawText() const;  
```  
  
## Return Value  
 Nonzero if a text label is displayed; otherwise 0.  
  
## Remarks  
 This method returns `FALSE` if the toolbar button has no associated text label ([CMFCToolBarButton::m_strText](../vs140/CMFCToolBarButton--m_strText.md) is empty) or [CMFCToolBarButton::m_bText](../vs140/CMFCToolBarButton--m_bText.md) is set to `FALSE`.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::m_strText](../vs140/CMFCToolBarButton--m_strText.md)   
 [CMFCToolBarButton::m_bText](../vs140/CMFCToolBarButton--m_bText.md)