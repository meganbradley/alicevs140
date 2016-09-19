---
title: "CMFCStatusBar::GetPaneWidth"
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
ms.assetid: e387ee8b-29c6-4b3f-bd0f-339ef4c77a28
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCStatusBar::GetPaneWidth
Retrieves the width of the pane of a status bar.  
  
## Syntax  
  
```  
int GetPaneWidth(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 [in] `nIndex`  
 Specifies the index of the status bar pane.  
  
## Return Value  
 The width of the status bar pane that `nIndex` specifies; otherwise, zero if a status-bar pane does not exist.  
  
## Requirements  
 **Header:** afxstatusbar.h  
  
## See Also  
 [CMFCStatusBar Class](../vs140/CMFCStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)