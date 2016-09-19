---
title: "CMFCToolTipCtrl::OnDrawLabel"
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
ms.assetid: 86a903db-dc59-4cb9-8799-8313d52d49df
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolTipCtrl::OnDrawLabel
Draws the label of a tooltip, or calculates the size of the label.  
  
## Syntax  
  
```  
virtual CSize OnDrawLabel(  
   CDC* pDC,  
   CRect rect,  
   BOOL bCalcOnly   
);  
```  
  
#### Parameters  
 `[in] pDC`  
 A pointer to a device context.  
  
 `[in] rect`  
 Bounding rectangle of the label area.  
  
 `[in] bCalcOnly`  
 If `TRUE`, the label will not be drawn.  
  
## Return Value  
 Size of the label, in pixels.  
  
## Remarks  
 Override this method in a derived class if you want to customize the appearance of the tooltip label.  
  
## Requirements  
 **Header:** afxToolTipCtrl.h  
  
## See Also  
 [CMFCToolTipCtrl Class](../vs140/CMFCToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)