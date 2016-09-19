---
title: "CMFCToolTipCtrl::OnDrawBorder"
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
ms.assetid: 96c3eba0-06d8-436a-ac10-7667a7c1ffab
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolTipCtrl::OnDrawBorder
Draws the border of a tooltip.  
  
## Syntax  
  
```  
virtual void OnDrawBorder(  
   CDC* pDC,  
   CRect rect,  
   COLORREF clrLine   
);  
```  
  
#### Parameters  
 `[in] pDC`  
 Pointer to a device context.  
  
 `[in] rect`  
 The bounding rectangle of the tooltip.  
  
 `[in] clrLine`  
 Border color.  
  
## Remarks  
 Override this method in a derived class to customize the appearance of the tooltip border.  
  
## Requirements  
 **Header:** afxToolTipCtrl.h  
  
## See Also  
 [CMFCToolTipCtrl Class](../vs140/CMFCToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)