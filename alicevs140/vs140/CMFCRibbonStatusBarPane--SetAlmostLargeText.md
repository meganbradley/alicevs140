---
title: "CMFCRibbonStatusBarPane::SetAlmostLargeText"
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
ms.assetid: ba9cbb06-356d-4f42-b21f-f21fba137562
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonStatusBarPane::SetAlmostLargeText
Define the longest text that can be displayed in the status bar pane without truncation.  
  
## Syntax  
  
```  
void SetAlmostLargeText(  
   LPCTSTR lpszAlmostLargeText   
);  
```  
  
#### Parameters  
 [in] `lpszAlmostLargeText`  
 Specifies the longest string that can be displayed on the status bar pane without truncation.  
  
## Remarks  
 The library calculates the size of text that `lpszAlmostLargeText` specifies and resizes the pane accordingly. The text will be truncated if it still does not fit in the pane.  
  
## Requirements  
 **Header:** afxribbonstatusbarpane.h  
  
## See Also  
 [CMFCRibbonStatusBarPane Class](../vs140/CMFCRibbonStatusBarPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)