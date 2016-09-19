---
title: "CMFCRibbonProgressBar::SetPos"
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
ms.assetid: b48459ba-6124-456c-adcb-a8de261e0e3c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonProgressBar::SetPos
Sets the current position of the progress bar.  
  
## Syntax  
  
```  
void SetPos(  
    int nPos,  
    BOOL bRedraw = TRUE  
);  
```  
  
#### Parameters  
 [in] `nPos`  
 Specifies the position to which the progress bar is set.  
  
 [in] `bRedraw`  
 Specifies whether the progress bar should be redrawn.  
  
## Remarks  
 The range being set must be within the range specified by the [CMFCRibbonProgressBar::SetRange](../vs140/CMFCRibbonProgressBar--SetRange.md) method.  
  
## Requirements  
 **Header:** afxRibbonProgressBar.h  
  
## See Also  
 [CMFCRibbonProgressBar Class](../vs140/CMFCRibbonProgressBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)