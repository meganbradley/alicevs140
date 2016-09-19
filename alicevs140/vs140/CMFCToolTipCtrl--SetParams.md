---
title: "CMFCToolTipCtrl::SetParams"
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
ms.assetid: 767c3211-16df-4854-900e-a64ef85fd17c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolTipCtrl::SetParams
Specifies the visual appearance of a tooltip by using a [CMFCToolTipInfo](../vs140/CMFCToolTipInfo-Class.md) object.  
  
## Syntax  
  
```  
void SetParams(  
   CMFCToolTipInfo* pParams   
);  
```  
  
#### Parameters  
 `[in] pParams`  
 Pointer to a [CMFCToolTipInfo](../vs140/CMFCToolTipInfo-Class.md) object that contains  the display parameters.  
  
## Remarks  
 Whenever the tooltip is displayed, it is drawn by using the colors and visual styles that `pParams` specifies. The value of `pParams` is stored in the protected member `m_Params`, which can be accessed by a derived class that overrides [CMFCToolTipCtrl::OnDrawBorder](../vs140/CMFCToolTipCtrl--OnDrawBorder.md), [CMFCToolTipCtrl::OnDrawIcon](../vs140/CMFCToolTipCtrl--OnDrawIcon.md), [CMFCToolTipCtrl::OnDrawLabel](../vs140/CMFCToolTipCtrl--OnDrawLabel.md), [CMFCToolTipCtrl::OnDrawSeparator](../vs140/CMFCToolTipCtrl--OnDrawSeparator.md), or [CMFCToolTipCtrl::OnFillBackground](../vs140/CMFCToolTipCtrl--OnFillBackground.md) to maintain the specified appearance.  
  
## Requirements  
 **Header:** afxToolTipCtrl.h  
  
## See Also  
 [CMFCToolTipCtrl Class](../vs140/CMFCToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)