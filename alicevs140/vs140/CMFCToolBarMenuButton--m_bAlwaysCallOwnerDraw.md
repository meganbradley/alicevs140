---
title: "CMFCToolBarMenuButton::m_bAlwaysCallOwnerDraw"
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
ms.assetid: c9be84bd-352a-4c43-82e8-0fd35ef31bbc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::m_bAlwaysCallOwnerDraw
Specifies whether the framework always calls [CFrameWndEx::OnDrawMenuImage](../vs140/CFrameWndEx--OnDrawMenuImage.md) when a button is drawn.  
  
## Syntax  
  
```  
static BOOL m_bAlwaysCallOwnerDraw;  
```  
  
## Remarks  
 When this member variable is set to `TRUE`, the button always calls [CFrmWndEx::OnDrawMenuImage](../vs140/CFrameWndEx--OnDrawMenuImage.md) method to display the image on the button. When `m_bAlwaysCallOwnerDraw` is `FALSE`, the button itself draws the image if the image is predefined. Otherwise, it calls `OnDrawMenuImage`.  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)