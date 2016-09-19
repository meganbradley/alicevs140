---
title: "CFrameWnd::SetMessageText"
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
ms.assetid: 50162bc5-c46f-434c-a4fc-f152b8d2d09d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::SetMessageText
Call this function to place a string in the status-bar pane that has an ID of 0.  
  
## Syntax  
  
```  
  
      void SetMessageText(  
   LPCTSTR lpszText   
);  
void SetMessageText(  
   UINT nID   
);  
```  
  
#### Parameters  
 `lpszText`  
 Points to the string to be placed on the status bar.  
  
 `nID`  
 String resource ID of the string to be placed on the status bar.  
  
## Remarks  
 This is typically the leftmost, and longest, pane of the status bar.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBar Class](../vs140/CStatusBar-Class.md)