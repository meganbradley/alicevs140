---
title: "CMFCRibbonBar::OnSysKeyDown"
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
ms.assetid: 9dea853a-c78c-43f6-b72b-b5ffa1056e44
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::OnSysKeyDown
Called by the framework when the user presses the F10 key or holds down the ALT key and then presses another key.  
  
## Syntax  
  
```  
BOOL OnSysKeyDown(  
   CFrameWnd* pFrameWnd,  
   WPARAM wParam,  
   LPARAM lParam  
);  
```  
  
#### Parameters  
 [in] `pFrameWnd`  
 Pointer to the parent main frame window of the ribbon bar.  
  
 [in] `wParam`  
 Virtual key code of the key being pressed.  
  
 [in] `lParam`  
 Keyboard state flags when the key was pressed.  
  
## Return Value  
 `TRUE` if the keystroke event was processed; otherwise `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)