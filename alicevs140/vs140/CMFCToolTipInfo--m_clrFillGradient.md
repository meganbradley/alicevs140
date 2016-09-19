---
title: "CMFCToolTipInfo::m_clrFillGradient"
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
ms.assetid: 79df80b4-86bb-4682-aa9a-63a26619b567
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolTipInfo::m_clrFillGradient
Specifies the end color for a gradient background for tooltips.  
  
## Syntax  
  
```  
COLORREF m_clrFillGradient;  
```  
  
## Remarks  
 If `m_clrFillGradient` is -1, there is no gradient. Otherwise, the gradient initial color is specified by [CMFCToolTipInfo::m_clrFill](../vs140/CMFCToolTipInfo--m_clrFill.md) and the gradient finish color is specified by `m_clrFillGradient`. [CMFCToolTipInfo::m_nGradientAngle](../vs140/CMFCToolTipInfo--m_nGradientAngle.md) determines the direction of the gradient.  
  
## Requirements  
 **Header:** afxToolTipCtrl.h  
  
## See Also  
 [CMFCToolTipInfo Class](../vs140/CMFCToolTipInfo-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)