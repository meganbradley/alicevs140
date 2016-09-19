---
title: "CMFCRibbonBar::OnSysKeyUp"
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
ms.assetid: da76ed47-c372-4ffd-8aa5-951a5df9c138
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::OnSysKeyUp
Called by the framework when the user releases the F10 key, the ALT key, or a key that was pressed when the ALT key was held down.  
  
## Syntax  
  
```  
BOOL OnSysKeyUp(  
   CFrameWnd* pFrameWnd,  
   WPARAM wParam,  
   LPARAM lParam  
);  
```  
  
#### Parameters  
 [in] `pFrameWnd`  
 Pointer to the parent main frame window of the ribbon bar.  
  
 [in] `wParam`  
 Virtual key code of the key being released.  
  
 [in] `lParam`  
 This parameter is not used.  
  
## Return Value  
 `TRUE` if the keystroke event was processed; otherwise `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)