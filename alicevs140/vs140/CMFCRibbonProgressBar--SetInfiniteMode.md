---
title: "CMFCRibbonProgressBar::SetInfiniteMode"
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
ms.assetid: 21e37101-414f-42dc-86e4-01490c6dc7d6
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonProgressBar::SetInfiniteMode
Sets the progress bar to work in infinite mode.  
  
## Syntax  
  
```  
void SetInfiniteMode(  
    BOOL bSet = TRUE  
);  
```  
  
#### Parameters  
 [in] `bSet`  
 `TRUE` to specify that the progress bar is in infinite mode; otherwise, `FALSE`.  
  
## Remarks  
 Usually, if the progress bar is in infinite mode, it is telling the user that an operation is ongoing, but that the completion time is unknown. Thus, the progress bar fills repeatedly from the minimum value to the maximum value.  
  
## Requirements  
 **Header:** afxRibbonProgressBar.h  
  
## See Also  
 [CMFCRibbonProgressBar Class](../vs140/CMFCRibbonProgressBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)