---
title: "CMFCToolTipInfo::m_bVislManagerTheme"
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
ms.assetid: ccaf0c43-0aa5-4ef3-a0e1-4f4c95d3d8fb
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolTipInfo::m_bVislManagerTheme
Specifies whether the visual manager of the application controls the appearance of all tooltips.  
  
## Syntax  
  
```  
BOOL m_bVislManagerTheme;  
```  
  
## Remarks  
 If `m_bVislManagerTheme` is `TRUE`, every tooltip requests a new [CMFCToolTipInfo](../vs140/CMFCToolTipInfo-Class.md) from the visual manager of the application before they appear on the screen, and uses the values in that object to determine their appearance. The other members of your [CMFCToolTipInfo](../vs140/CMFCToolTipInfo-Class.md) are ignored.  
  
## Requirements  
 **Header:** afxToolTipCtrl.h  
  
## See Also  
 [CMFCToolTipInfo Class](../vs140/CMFCToolTipInfo-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)