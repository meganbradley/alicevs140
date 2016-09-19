---
title: "CMFCAutoHideBar::RemoveAutoHideWindow"
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
ms.assetid: 0787d005-5ff8-4d78-8952-bd7310599e88
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCAutoHideBar::RemoveAutoHideWindow
Removes and destroys the auto-hide window.  
  
## Syntax  
  
```  
 BOOL RemoveAutoHideWindow(  
		    CDockablePane* pAutoHideWnd  
		);   
```  
  
#### Parameters  
 CDockablePane* `pAutoHideWnd`  
 The auto-hide window to remove.  
  
## Return Value  
 TRUE if successful; otherwise FALSE.  
  
## Remarks  
  
## Requirements  
 **Header:** afxautohidebar.h  
  
## See Also  
 [CMFCAutoHideBar Class](../vs140/CMFCAutoHideBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)