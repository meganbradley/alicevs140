---
title: "CMFCToolTipInfo::m_clrFill"
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
ms.assetid: 44ff36f1-5e3c-4705-9de4-d6c5e4cb2149
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolTipInfo::m_clrFill
Specifies the color of tooltip backgrounds.  
  
## Syntax  
  
```  
COLORREF m_clrFill;  
```  
  
## Remarks  
 If [CMFCToolTipInfo::m_clrFillGradient](../vs140/CMFCToolTipInfo--m_clrFillGradient.md) is -1, the tooltip background color is `m_clrFill`. Otherwise, `m_clrFill` specifies the color of the beginning of the gradient and `m_clrFillGradient` specifies the color of the end of the gradient. [CMFCToolTipInfo::m_nGradientAngle](../vs140/CMFCToolTipInfo--m_nGradientAngle.md) determines the direction of the gradient.  
  
## Requirements  
 **Header:** afxToolTipCtrl.h  
  
## See Also  
 [CMFCToolTipInfo Class](../vs140/CMFCToolTipInfo-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)