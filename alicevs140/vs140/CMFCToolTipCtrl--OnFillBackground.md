---
title: "CMFCToolTipCtrl::OnFillBackground"
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
ms.assetid: 292dabac-d2c8-4f97-a443-c3aa6188d91e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolTipCtrl::OnFillBackground
Fills the tooltip background.  
  
## Syntax  
  
```  
virtual void OnFillBackground(  
   CDC* pDC,  
   CRect rect,  
   COLORREF& clrText,  
   COLORREF& clrLine   
);  
```  
  
#### Parameters  
 `[in] pDC`  
 A pointer to a device context.  
  
 `[in] rect`  
 Specifies the bounding rectangle of the area to fill.  
  
 `[in] clrText`  
 Tooltip foreground color.  
  
 `[in] clrLine`  
 Color of borders and the delimiter line between label and description.  
  
## Remarks  
 The default implementation fills the rectangle that is specified by `rect` with the color or pattern specified by the most recent call to [CMFCToolTipCtrl::SetParams](../vs140/CMFCToolTipCtrl--SetParams.md).  
  
 Override this method in a derived class if you want to customize the appearance of the tooltip.  
  
## Requirements  
 **Header:** afxToolTipCtrl.h  
  
## See Also  
 [CMFCToolTipCtrl Class](../vs140/CMFCToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)