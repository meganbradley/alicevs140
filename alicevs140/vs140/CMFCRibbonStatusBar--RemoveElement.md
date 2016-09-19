---
title: "CMFCRibbonStatusBar::RemoveElement"
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
ms.assetid: 2d707446-1423-401b-b10a-aeb3e9d669ac
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonStatusBar::RemoveElement
Removes the element that has a specified command ID from the ribbon status bar.  
  
## Syntax  
  
```  
BOOL RemoveElement(  
   UINT uiID   
);  
```  
  
#### Parameters  
 [in] `uiID`  
 The ID of the element to remove from the status bar.  
  
## Return Value  
 `TRUE` if an element with the specified `uiID` is removed. `FALSE` otherwise.  
  
## Requirements  
 **Header:** afxribbonstatusbar.h  
  
## See Also  
 [CMFCRibbonStatusBar Class](../vs140/CMFCRibbonStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)