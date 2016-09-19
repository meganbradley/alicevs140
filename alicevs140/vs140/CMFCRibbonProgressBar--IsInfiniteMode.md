---
title: "CMFCRibbonProgressBar::IsInfiniteMode"
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
ms.assetid: 1f989b77-6c46-497c-9ba9-c8775c273ee1
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonProgressBar::IsInfiniteMode
Specifies whether the progress bar is working in infinite mode.  
  
## Syntax  
  
```  
BOOL IsInfiniteMode() const;  
```  
  
## Return Value  
 `TRUE` if the progress bar is in infinite mode; otherwise, `FALSE`.  
  
## Remarks  
 In infinite mode, the progress bar fills repeatedly from the minimum value to the maximum value. You might use infinite mode to indicate that an operation is ongoing, but that the completion time is unknown.  
  
## Requirements  
 **Header:** afxRibbonProgressBar.h  
  
## See Also  
 [CMFCRibbonProgressBar Class](../vs140/CMFCRibbonProgressBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)