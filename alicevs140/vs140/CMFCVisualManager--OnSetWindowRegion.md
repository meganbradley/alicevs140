---
title: "CMFCVisualManager::OnSetWindowRegion"
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
ms.assetid: f219e031-3710-4c04-a4e8-155ad60475a4
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnSetWindowRegion
The framework calls this method after it sets a region that contains frames and pop-up menus.  
  
## Syntax  
  
```  
virtual BOOL OnSetWindowRegion(  
   CWnd* pWnd,  
   CSize sizeWindow  
);  
```  
  
#### Parameters  
 [in] `pWnd`  
 A pointer to the window with the region that changed.  
  
 [in] `sizeWindow`  
 The size of the window.  
  
## Return Value  
 `TRUE` if the method is successful; `FALSE` otherwise.  
  
## Remarks  
 The framework calls this method to notify the visual manager that a region has been set for frames and pop-up menus. For more information, see [CWindow::SetWindowRgn](../vs140/CWindow--SetWindowRgn.md).  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWindow::SetWindowRgn](../vs140/CWindow--SetWindowRgn.md)